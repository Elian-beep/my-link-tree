<template>
  <footer class="footer" :class="{ 'themeDark': isDark }">
    <p class="title-tec"></p>
    <!-- <div class="icons-tec">
      <IconTec name-icon="fa-brands fa-html5" font-color="#FF0000" />
      <IconTec name-icon="fa-brands fa-css3" fontColor="#00BFFF" />
      <IconTec name-icon="fa-brands fa-git" font-color="#FF8C00" />
      <IconTec name-icon="fa-brands fa-bootstrap" font-color="#4B0082" />
      <IconTec name-icon="fa-brands fa-node" font-color="#3CB371" />
      <IconTec name-icon="fa-brands fa-js" font-color="#FFD700" />
      <IconTec name-icon="fa-brands fa-vuejs" font-color="#66CDAA" />
      <IconTec name-icon="fa-brands fa-react" font-color="#00BFFF" />
      <IconTec name-icon="fa-brands fa-java" font-color="#FFD700" />
    </div> -->
    <p class="credits">Desenvolvido por Elian Batista</p>
  </footer>
</template>
  
<script lang="ts">
import { defineComponent } from "vue";
import IconTec from "./IconTec.vue";

export default defineComponent({
  name: "FooterPage",
  components: {  },
  props: {
    isDark: {
      type: Boolean,
      required: true,
    },
  },
});
</script>
  
<style scoped>
footer {
  margin-top: 22px;
  margin-bottom: 8px;

  --color: #636363;
}

footer.themeDark {
  --color: #d3d3d3;
}

p {
  color: var(--color);
}

.title-tec {
  text-align: center;
  border-top: 1px solid var(--color);
  width: 85%;
  margin: 0 auto;
  padding-top: 8px;
  font-size: 10pt;
}
.icons-tec {
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: space-evenly;
  gap: 0 6px;
  width: 30%;
  margin: 0 auto;
  flex-wrap: wrap;
}

.credits {
  font-size: 10pt;
  margin-top: 8px;
  text-align: center;
}
</style>
  