<template>
  <li>
    <img :src="image"/>
    <slot></slot>
  </li>
</template>

<script>
export default {
    name: "CardComponent",
    data() {
      return {
        image: "https://cdn-icons-png.flaticon.com/128/326/326370.png"
      }
    }
}
</script>

<style scoped>
    li {
        margin: 1rem;
        font-size: 1.25rem;
        font-weight: bold;
        background: purple;
        padding: 0.5rem;
        color: #1f1f1f;
        border-radius: 25px;
    }
    img {
      width: 100px;
      height: 100px;
    }
</style>