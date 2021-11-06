<template>
  <div>
    Some shared layout content:
    <slot name="header">default</slot>
  </div>
</template>

<script>
export default {
 layout: "custom"
};
</script>