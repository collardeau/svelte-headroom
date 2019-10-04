# Svelte-Headroom

Hide your header until you need it! 

Svelte Headroom is a Svelte Component to hide or show your header on scroll.

This package has no dependencies.

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

### Duration

You can change the duration of the sliding effect by passing a `duration` prop such as `"500ms"`. That value is passed on as a [CSS Transition Duration](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-duration). The default value is `"300ms"`.

```html

<Headroom duration='500ms'>
  <!-- my header -->
</Headroom>

```

### Offset

You can change the `offset` so the effect doesn't trigger until you've scrolled down a set amout of pixels. The default value is `0`.

```html

<Headroom offset={50}>
  <!-- my header -->
</Headroom>

```
