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
        props: ["employees"],
        data() {
            return {
                message: "แสดงรายชื่อพนักงานทุกคน"
            }
        }
    }
</script>