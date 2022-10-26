<template>
  <footer>
    <p class="title-tec">Tecnologias</p>
    <div class="icons-tec">
        <IconTec name-icon="fa-brands fa-html5" font-color="#FF0000" />
        <IconTec name-icon="fa-brands fa-css3" fontColor="#00BFFF" />
        <IconTec name-icon="fa-brands fa-git" font-color="#FF8C00" />
        <IconTec name-icon="fa-brands fa-js" font-color="#FFD700" />
        <IconTec name-icon="fa-brands fa-bootstrap" font-color="#4B0082" />
        <IconTec name-icon="fa-brands fa-vuejs" font-color="#66CDAA" />
        <IconTec name-icon="fa-brands fa-node" font-color="#3CB371" />
        <IconTec name-icon="fa-brands fa-react" font-color="#00BFFF" />
    </div>
  </footer>
</template>
  
<script lang="ts">
import { defineComponent } from "vue";
import IconTec from "./IconTec.vue";

export default defineComponent({
  name: "FooterPage",
  components: { IconTec }
});
</script>
  
<style scoped>
footer{
    margin-top: 22px;
}

.title-tec{
    text-align: center;
    border-top: 1px solid #000;
    width: 85%;
    margin: 0 auto;
    padding-top: 5px;
}
.icons-tec{
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: space-evenly;
    gap: 6px;
    width: 85%;
    margin: 0 auto;
    flex-wrap: wrap;
}
</style>
  