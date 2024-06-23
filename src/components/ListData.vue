<template>
    <div> {{ message }} </div>
    <PersonComponent name="ก้อง" salary=30000></PersonComponent>
    <PersonComponent name="โจ้" salary=20000></PersonComponent>
    <PersonComponent name="เจมส์" salary=15000 ></PersonComponent>
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
                message: "แสดงรายชื่อพนักงานทุกคน"
            }
        }
    }
</script>