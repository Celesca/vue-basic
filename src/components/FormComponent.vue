<template>
    <form>
        <div class="form-control">
            <label for="emp-name">ชื่อพนักงาน</label>
            <input type="text" v-model.trim="employee.name"/>
        </div>
        <div class="form-control">
            <label for="salary">เงินเดือน</label>
            <input type="number" v-model="employee.salary"/>
        </div>
        <div>
            <button>บันทึกข้อมูล</button>
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

<style scoped>
    form {
        margin: 2rem auto;
        max-width: 40rem;
        border-radius: 12px;
        box-shadow: 0 2px 10px rgba(0,0,0,0.26);
        padding: 2rem;
        background: #fff;
    }

    .form-control {
        margin: 0.5rem 0;
    }
    label {
        font-weight: bold;
    }
    input {
        display: block;
        width: 100%;
        font: inherit;
        padding: 0.5rem;
    }
    button {
        font:inherit;
        background-color: orangered;
        color: white;
        cursor: pointer;
        padding: 0.5rem 1rem;
        border-radius: 15px;
    }
</style>