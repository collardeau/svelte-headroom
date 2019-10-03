# Svelte-Headroom

#### Hide your header until you need it!

Svelte  Headroom is a Svelte Component to hide or show your header on scroll.

## Demo

[Code Sandbox](https://codesandbox.io/embed/svelte-headroom-demo-cf7lv)

# Install

`npm install svelte-headroom`

# Usage

```html
<script>
  import Headroom from "svelte-headroom";
</script>

<Headroom>
  <header>
    My Header
  </header>
</Headroom>

```

# Options

You can change the duration of the sliding effect by passing a `duration` prop such as `500ms`;

```html

<Headroom duration='500ms'>
  <!-- my header -->
</Headroom>


```
