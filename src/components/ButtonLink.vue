<template>
    <button @click="redirectLink">
        <i></i>
        <span>{{textButton}}</span>
    </button>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'ButtonLink',
    props: {
        textButton: {
            type: String,
            required: true
        },
        inputLink: {
            type: String,
            required: true
        }
    },
    methods: {
        redirectLink() {
            console.log('redirecionando para: ', this.inputLink);
            window.location.assign(this.inputLink);
        }
    }
});
</script>

<style scoped>

button{
    border: 1px solid #213140;
    background: none;
    width: 85%;
    height: 35px;
    border-radius: 4px;

    display: flex;
    justify-content: center;
    align-items: center;

    color: #213140;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 1px;

    transition: ease-in .2s;
}

button:hover{
    background: #213140;
    color: rgb(246, 246, 246);
    cursor: pointer;
}
</style>