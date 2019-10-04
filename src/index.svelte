<script>
  export let duration = "300ms";
  export let offset = 0;

  let headerClass = "pin";
  let y = 0;
  let lastY = 0;

  function deriveClass(y, dir) {
    if (y < offset) return "pin";
    if (dir === "up") return "pin";
    if (dir === "down") return "unpin";
    return headerClass;
  }

  function updateClass(y) {
    const dir = lastY - y < 0 ? "down" : "up";
    const result = deriveClass(y, dir);
    lastY = y;
    return result;
  }

  function action(node) {
    node.style.transitionDuration = duration;
  }

  $: headerClass = updateClass(y);
</script>

<style>
  div {
    position: fixed;
    width: 100%;
    top: 0;
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
