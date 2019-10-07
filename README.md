# Svelte-Headroom

**Hide your header until you need it!**

Svelte Headroom is a [Svelte](https://svelte.dev) component to hide or show your header on scroll, inspired by [headroom.js](https://wicky.nillia.ms/headroom.js/)

`svelte-headroom` has **no dependencies**.

# Demo

[Code Sandbox](https://codesandbox.io/embed/svelte-headroom-demo-cf7lv)

# Install

`npm install svelte-headroom`

# Usage

```html
<script>
  import Headroom from "svelte-headroom";
</script>

<Headroom>
  <!-- my header -->
</Headroom>

```

# Props


### `offset` number

The number of pixels from the top of the page before the effect is allowed to occur. The default value is `0`.

```html

<Headroom offset={50}>
  <!-- my header -->
</Headroom>

```

### `tolerance` number

The amount of pixels that need to be scrolled in either direction for the effect to occur. This is useful if you want the user to be able to scroll slowly and not change the header position. The default value is `0`.

```html

<Headroom tolerance={10}>
  <!-- my header -->
</Headroom>

```

### `duration` string

The duration of the sliding effect. The value is passed on as a [CSS Transition Duration](https://developer.mozilla.org/en-US/docs/Web/CSS/transition-duration). The default value is `"300ms"`.

```html

<Headroom duration='500ms'>
  <!-- my header -->
</Headroom>

```

# Events

A `svelte-headroom` component emits two events: `pin` and `unpin`.

```jsx
<Headroom
  on:pin={ () => {} }
  on:unpin={ () => {} }
>
  <header>My Header</header>
</Headroom>
```

Happy Coding!
