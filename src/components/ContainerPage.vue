<template>
  <div class="container" :class="{ 'themeDark': isDark }">
    <ContentPage @alterTheme="switchTheme">

    </ContentPage>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ContentPage from "./ContentPage.vue";

export default defineComponent({
  name: "ContainerPage",
  components: { ContentPage },
  data() {
    return{
      isDark: false
    }
  },
  methods: {
    switchTheme(isDark : boolean){
      this.isDark = isDark;
      console.log(`Tema no container: ${this.isDark}`);
      
    }
  }
});
</script>

<style scoped>
div{
  --bg: #e4e3e3;
}

div.themeDark{
  --bg: #636363;
}
.container {
  height: 100vh;
  max-width: 100vw;

  background: var(--bg);

  display: flex;
  align-items: center;
  justify-content: center;
}
</style>