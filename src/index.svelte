<script>
  import { headroom } from "headroom";
  export let options = null;

  function action(node) {
    const hr = new headroom(node, options);
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
