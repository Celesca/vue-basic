<template>
    <div> {{ message }} </div>
    <PersonComponent></PersonComponent>
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