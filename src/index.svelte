<script>
  import Headroom from "headroom.js";
  export let options = null;

  function action(node) {
    const hr = new Headroom(node, options);
    hr.init();
    return {
      destroy() {
        hr.destroy();
      }
    };
  }
</script>

<div use:action>
  <slot />
</div>
