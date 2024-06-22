<template>
  <section>
    <img :src="picture" :width="size" :height="size" alt=""/>
    <h1>ชื่อผู้สมัคร : {{  getFullName() }}</h1>
    <h2>{{ 500 + 200 }}</h2>
    <h2>อายุ : {{ age }}</h2>
    <h2>ที่อยู่ : <span v-html="address"></span></h2>
    <p> Social : <a :href="social" target="_blank">Facebook</a></p>
    <p>งานอดิเรก</p>
    <ul>
      <li>{{ hobby[0] }}</li>
      <li>{{ hobby[1] }}</li>
      <li>{{ hobby[2] }}</li>
    </ul>

    <p>ข้อมูลทั่วไป</p>
    <ul>
      <li>เพศ : {{  general.gender }} </li>
      <li>ส่วนสูง : {{  general.height }} เซนติเมตร</li>
      <li>น้ำหนัก : {{  general.weight }} กิโลกรัม</li>
      <li>สถานะ : {{  general.status }} </li>
    </ul>
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
        address: "<i>กรุงเทพมหานคร</i>",
        picture: "https://cdn-icons-png.flaticon.com/128/16770/16770369.png",
        size: 50,
        social: "https://www.facebook.com/kongruksiamtutorial",
        hobby: ["เล่นเกม", "อ่านหนังสือ", "เขียนโปรแกรม"],
        general: {
          gender: "ชาย",
          height: 170,
          weight: 60,
          status: false
        }
      }
    },
    methods: {
      getFullName() {
        return `${this.firstName} ${this.lastName}`
      }
    }
  }
</script>

