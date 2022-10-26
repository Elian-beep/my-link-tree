<template>
    <button @click="redirectLink">
        <i :class="icone"></i>
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
        },
        icone: {
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
    border: 1.5px solid #213140;
    background: none;
    width: 85%;
    height: 40px;
    border-radius: 4px;

    display: flex;
    justify-content: space-around;
    align-items: center;

    color: #213140;
    font-weight: 500;
    font-size: 10.5pt;
    text-decoration: none;
    text-transform: uppercase;
    letter-spacing: 1px;

    transition: ease-in-out .25s;
}

button i{
    font-size: 11pt;
}

button span{
    width: 50%;
    text-align: start;
}

button:hover{
    background: #213140;
    color: rgb(246, 246, 246);
    cursor: pointer;
}
</style>