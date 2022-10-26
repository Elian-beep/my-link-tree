<template>
  <div>
    <ButtonLink textButton="Portifólio" inputLink="https://cursos.alura.com.br/vitrinedev/elian-19batista"/>
    <ButtonLink textButton="Github" inputLink="https://github.com/Elian-beep" />
    <ButtonLink textButton="Linkedin" inputLink="https://www.linkedin.com/in/elian-batista-beep/" />
    <ButtonLink textButton="E-mail" inputLink="mailto:elian.19batista@gmail.com" />
    <ButtonLink textButton="Instagram" inputLink="https://www.instagram.com/e_lianb/" />
  </div>
</template>
  
<script lang="ts">
import { defineComponent } from "vue";
import ButtonLink from "./ButtonLink.vue";

export default defineComponent({
  name: "BodyPage",
  components: { ButtonLink }
});
</script>
  
<style scoped>
div{
    margin-top: 22px;
    gap: 16px;
    display: flex;
    flex-direction: column;
    align-items: center;
}
</style>
  