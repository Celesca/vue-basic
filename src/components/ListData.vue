<template>
    <div> {{ message }} </div>
    <ul>
        <PersonComponent v-for="item in employees" :id="item.id" :key="item.id" :name="item.name" :salary="item.salary"
            :department="item.department" :isVisible="item.isVisible"
            @show="toggleVisible" @delete="removeEmployee"
            ></PersonComponent>
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
                { id: 1, name: "ก้อง", salary: 30000, department: "โปรแกรมเมอร์", isVisible: false },
                { id: 2, name: "โจ้", salary: 20000, department: "การตลาด", isVisible: false },
                { id: 3, name: "เจมส์", salary: 15000, department: "บัญชี", isVisible: false },
                { id: 4, name: "ซีโร่", salary: 12000, department: "การตลาด", isVisible: false },
                { id: 5, name: "ตุ๊ก", salary: 25000, department: "โปรแกรมเมอร์", isVisible: false },
            ]
        }
    },
    methods: {
        toggleVisible(id) {
            this.employees = this.employees.map((item) => {
                if (item.id === id) {
                    return {...item, isVisible: !item.isVisible }
                }
                return item
            })
        },
        removeEmployee(id) {
            this.employees = this.employees.filter(item => {
                return item.id !== id
            })
        }
    }
}
</script>

<style scoped>
    ul {
        list-style-type: none;
        margin: 1rem;
        padding: 0;
    }
</style>