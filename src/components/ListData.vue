<template>
    <div> {{ message }} </div>
    <ul>
       <PersonComponent v-for="(item, index) in employees" :key="index"
       :name="item.name" :salary="item.salary"></PersonComponent>
    </ul>
</template>

<script>
    import PersonComponent from './Person.vue'

    export default {
        name: "ListData",
        components: {
            PersonComponent
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