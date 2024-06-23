<template lang="">
    <CardComponent>
        <template v-slot:card-header>
            <h1> {{ name }}</h1>
        </template>

    <template v-slot:card-content>
        <p>เงินเดือน : {{ salary }} , ตำแหน่งงาน : {{ department }}</p>
        <p>เพศ : {{ gender }}</p>
        <p>ทักษะด้านภาษา : {{ skill }}</p>
    </template>
    </CardComponent>
</template>


<script>
import CardComponent from "./CardComponent.vue";
export default {
    name: "NewPerson",
    components: {
        CardComponent,
    },
    props: {
        name: {
            type: String,
            required: true,
        },
        salary: {
            type: Number,
            default: 15000,
        },
        department: {
            type: String,
            required: true,
        },
        gender: {
            type: String,
            required: true,
        },
        skill: {
            type: Array,

        }
    },
};
</script>
<style scoped>
p {
    color: white;
}
h1 {
    color: white;
}

button {
    font: inherit;
    cursor: pointer;
    border: 1px solid #ff0077;
    background: #ff0077;
    color: white;
    padding: 0.5rem 1rem;
    border-radius: 25px;
    box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
}

.fade-enter-from {
    opacity: 0;
}

.fade-enter-active {
    transition: all 0.5s linear;
}
</style>