<script>
  let headerClass = "pin";
  let lastDirection = "up";
  let y = 0;
  let lastY = 0;

  export let duration = "300ms";

  function changeClass(y) {
    let result = headerClass;
    const scrollDirection = lastY - y < 0 ? "down" : "up";
    const changedDirection = scrollDirection !== lastDirection;
    if (changedDirection) {
      result = scrollDirection === "down" ? "unpin" : "pin";
      lastDirection = scrollDirection;
    }
    lastY = y;
    return result;
  }

  function action(node) {
    node.style.transitionDuration = duration;
  }

  $: headerClass = changeClass(y);
</script>

<style>
  div {
    position: fixed;
    width: 100%;
    top: 0;
    /* will-change: transform; */
    transition: transform 300ms linear;
  }
  .pin {
    transform: translateY(0%);
  }
  .unpin {
    transform: translateY(-100%);
  }
</style>

<svelte:window bind:scrollY={y} />

<div use:action class={headerClass}>
  <slot />
</div>
