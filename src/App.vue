<template>
  <div>
    <h1 class="heading">App Component</h1>
  </div>
  <FormComponent></FormComponent>
  <ListData :employees="employees"></ListData>
</template>

<script>
import ListData from './components/ListData.vue'
import FormComponent from './components/FormComponent.vue'

  export default {
    name:"App",
    components: {
      ListData,
      FormComponent
    },
    data() {
      return {
        employees: [
          {name:"ก้อง", salary:30000},
          {name:"โจ้", salary:20000},
          {name:"เจมส์", salary:15000},
          {name:"ซีโร่"},
          {name:"ตุ๊ก", salary:25000}
        ]
      }
    }
  }

</script>

<style>
.heading {
  color: red;
  text-align: center;
}
</style>