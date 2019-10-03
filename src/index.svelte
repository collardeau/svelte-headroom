<script>
  import Headroom from "headroom";
  export let options = null;

  function headroom(node) {
    const hr = new Headroom(node, options);
    hr.init();
    return {
      destroy() {
        hr.destroy();
      }
    };
  }
</script>

<div use:headroom>
  <slot />
</div>
