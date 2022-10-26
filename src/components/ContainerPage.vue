<template>
  <div class="container">
    <ContentPage>

    </ContentPage>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ContentPage from "./ContentPage.vue";

export default defineComponent({
  name: "ContainerPage",
  components: { ContentPage }
});
</script>

<style scoped>
.container {
  height: 100vh;
  max-width: 100vw;

  background: #1C1C1C;

  display: flex;
  align-items: center;
  justify-content: center;
}
</style>