<template>
  <section :class="{ 'themeDark': isDark }">
    <ImageProfile />
    <h1>Elian Batista</h1>
    <p>Desenvolvedor Web</p>
    <p>Graduado em Ciência da Computação</p>
  </section>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ImageProfile from "./ImageProfile.vue";

export default defineComponent({
  name: "HeaderPage",
  components: { ImageProfile },
  props: {
    isDark: {
      type: Boolean,
      required: true
    }
  }
});
</script>

<style scoped>
section{
  --text-title: #213140;
  --text-subtitle: #636363;
  margin-top: 30px;
}

section.themeDark{
  --text-title: rgb(246, 246, 246);
  --text-subtitle: #d3d3d3;
}

h1 {
  font-size: 20pt;
  font-weight: 700;
  color: var(--text-title);
  text-align: center;
  margin-top: 12px;
}

p{
    font-size: 12pt;
    color: var(--text-subtitle);
    text-align: center;
    margin: 12px 22px 0 22px;
    font-weight: 300;
}

@media screen and (min-width: 500px) {
    h1{
        font-size: 22pt;
    }
}
</style>
