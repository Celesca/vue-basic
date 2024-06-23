<template>
    <ul>
        <NewPerson v-for="(item, index) in employees" :key="index"
        :name="item.name" :salary="item.salary" :department="item.department"
        :gender="item.gender" :skill="item.skill"/>
    </ul>
</template>

<script>
import NewPerson from './NewPerson.vue'

export default {
    name: "NewListData",
    components: {
        NewPerson,
    },
    props: [
        "employees"
    ]
}
</script>

<style scoped>
    ul {
        list-style-type: none;
        margin: 1rem;
        padding: 0;
    }
</style>