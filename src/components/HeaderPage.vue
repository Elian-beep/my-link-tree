<template>
  <section :class="{ 'themeDark': isDark }">
    <ImageProfile />
    <h1>Elian Batista</h1>
    <p>
      Desenvolvedor Front End, estudando e se aventurando no Back End, Cursando Ciência da
      Computação na UEA.
    </p>
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
}

section.themeDark{
  --text-title: #ddeeff;
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
