<template>
  <section>
    <h1>ชื่อผู้สมัคร : {{firstName}} {{ lastName }}</h1>
    <h2>{{ 500 + 200 }}</h2>
    <h2>อายุ : {{ age }}</h2>
  </section>

</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        firstName: "Kong",
        lastName:"Ruksiam",
        age:15
      }
    }
  }
</script>

