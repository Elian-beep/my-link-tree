<template>
  <div>
    <ButtonLink :isDark="isDark" textButton="Portifólio" icone="fa-regular fa-folder" inputLink="https://cursos.alura.com.br/vitrinedev/elian-19batista"/>
    <ButtonLink :isDark="isDark" textButton="Github" icone="fa-brands fa-github" inputLink="https://github.com/Elian-beep" />
    <ButtonLink :isDark="isDark" textButton="Linkedin" icone="fa-brands fa-linkedin" inputLink="https://www.linkedin.com/in/elian-batista-beep/" />
    <ButtonLink :isDark="isDark" textButton="E-mail" icone="fa-regular fa-envelope" inputLink="mailto:elian.19batista@gmail.com" />
    <ButtonLink :isDark="isDark" textButton="Instagram" icone="fa-brands fa-instagram" inputLink="https://www.instagram.com/e_lianb/" />
  </div>
</template>
  
<script lang="ts">
import { defineComponent } from "vue";
import ButtonLink from "./ButtonLink.vue";

export default defineComponent({
  name: "BodyPage",
  components: { ButtonLink },
  props: {
    isDark: {
      type: Boolean,
      required: true
    }
  }
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
  