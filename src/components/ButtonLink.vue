<template>
    <a href="#">
        Portifólio
    </a>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name: 'ButtonLink',
});
</script>

<style scoped>

a{
    border: 1px solid #213140;
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

a:hover{
    background: #213140;
    color: rgb(246, 246, 246);
}
</style>