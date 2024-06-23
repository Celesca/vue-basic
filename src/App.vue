<template>
  <header>
    <h1>ระบบจัดการข้อมูลพนักงาน</h1>
  </header>
  <div class="show-button-container">
  <button class="show-button" @click="toggleShowForm">เพิ่มพนักงานใหม่</button>
</div>
  <div v-show="isShowForm">
  <form-component></form-component>
</div>
  <section class="employee-content">
    <h2>ข้อมูลพนักงาน</h2>
    <ListData/>
  </section>
</template>

<script>

import FormComponent from './components/FormComponent.vue'
import ListData from './components/ListData.vue'

  export default {
    name:"App",
    components: {
      ListData,
      FormComponent
    },
    data () {
      return {
        isShowForm: false
      }
    },
    methods: {
      toggleShowForm() {
        this.isShowForm = !this.isShowForm
      
      }
    }
  }

</script>

<style>
* {
  box-sizing: border-box;
}

body {
  margin:0;
}

header {
  box-shadow: 0 2px 8px rgba(0,0,0, 0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  background-color: purple;
  color: white;
  text-align: center;
}

.employee-content {
  box-shadow: 0 2px 8px rgba(0,0,0,0.26);
  margin: 3rem;
  border-radius: 10px;
  padding: 1rem;
  text-align: center;
}

.employee-content h2 {
  font-size: 2rem;
  border-bottom: 4px solid #ccc;
  color: purple;
  margin: 0 0 1rem 0;
}

.show-button-container {
  display: flex;
  justify-content: center;
}

.show-button {
  padding: 0.5rem 1rem;
  background-color: purple;
  color: white;
  border: none;
  border-radius: 10px;
  cursor: pointer;
}
</style>