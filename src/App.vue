<template>
  <div>
    <h1 class="heading">App Component</h1>
  </div>
  <FormComponent></FormComponent>
  <ListData></ListData>
</template>

<script>
import ListData from './components/ListData.vue'
import FormComponent from './components/FormComponent.vue'

  export default {
    name:"App",
    components: {
      ListData,
      FormComponent
    }
  }

</script>

<style>
.heading {
  color: red;
  text-align: center;
}
</style>