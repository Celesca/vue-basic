<template>
  <section>
    <img :src="picture" :width="size" :height="size" alt="icon" ref="imageEl"/>
    <br/>
    <form @submit.prevent="handleSubmit">
      <label>ป้อนชื่อเล่น</label>
      <input type="text" ref="nickNameEl"/>

      <button type="submit">บันทึก</button>
    </form>
    <h1>ชื่อผู้สมัคร : {{  getFullName() }}</h1>
    <h1>ชื่อเล่น : {{ nickname }}</h1>
    <h2>{{ 500 + 200 }}</h2>
    <h2>อายุ : {{ age }}</h2>
    <h2>ที่อยู่ : <span v-html="address"></span></h2>
    <p> Social : <a :href="social" target="_blank">Facebook</a></p>
    <p v-if="hobby.length === 0">ไม่มีงานอดิเรก</p>
    <div v-else>
      <p>งานอดิเรก</p>
      <ul>
          <li v-for="(item,index) in hobby" :key="index">{{ index }} - {{ item }}</li>
      </ul>
    </div>

    <p>ข้อมูลทั่วไป</p>
    <ul>
      <li>เพศ : {{  general.gender }} </li>
      <li>ส่วนสูง : {{  general.height }} เซนติเมตร</li>
      <li>น้ำหนัก : {{  general.weight }} กิโลกรัม</li>
      <li>สถานะ : {{  general.status }} </li>
    </ul>
    <button @click="showData()">คลิกเพื่อคำนวณ</button>
    <div>
      <button @click.ctrl="increment(10)">เพิ่ม</button>
      <button @click.middle="decrement(3)" @click.left="decrement(1)">ลด</button>
      </div>
  </section>

</template>

<script>
  export default {
    name: 'App',
    data() {
      return {
        firstName: "Kong",
        lastName:"Ruksiam",
        nickname:"",
        age:15,
        address: "<i>กรุงเทพมหานคร</i>",
        picture: "https://cdn-icons-png.flaticon.com/128/16770/16770369.png",
        size: 50,
        social: "https://www.facebook.com/kongruksiamtutorial",
        hobby: ["เล่นเกมส์", "อ่านหนังสือ", "เล่นกีฬา"],
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
      },
      showData() {
        alert(this.getFullName())
      },
      increment(value) {
        this.age += value
      },
      decrement(value) {
        this.age -= value
      },
      setNickname(event) {
        this.nickname = event.target.value
      },
      handleSubmit() {
        this.nickname = this.$refs.nickNameEl.value;
      }
    }
  }
</script>

