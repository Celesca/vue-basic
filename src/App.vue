<template>
  <section>
    <h1>ชื่อผู้สมัคร : {{  getFullName() }}</h1>
    <h2>{{ 500 + 200 }}</h2>
    <h2>อายุ : {{ age }}</h2>
    <h2>ที่อยู่ : <span v-html="address"></span></h2>
  </section>

</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        firstName: "Kong",
        lastName:"Ruksiam",
        age:15,
        address: "<i>กรุงเทพมหานคร</i>"
      }
    },
    methods: {
      getFullName() {
        return `${this.firstName} ${this.lastName}`
      }
    }
  }
</script>

