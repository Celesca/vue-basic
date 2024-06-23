<template>
    <form>
        <div class="form-control">
            <label for="emp-name">ชื่อพนักงาน</label>
            <input type="text" v-model="employee.name"/>

        </div>
    </form>
</template>


<script>
export default {
    name:"FormComponent",
    data() {
        return {
            employee: {
                name: "kongruksiam",
                salary: 15000,
            }
        }
    }
}

</script>

<style>

</style>