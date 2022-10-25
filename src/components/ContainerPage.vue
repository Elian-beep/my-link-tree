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

  background: linear-gradient(
    0deg,
    rgba(0, 0, 0, 1) 0%,
    rgba(152, 153, 153, 1) 34%,
    rgba(249, 249, 249, 1) 75%
  );

  display: flex;
  align-items: center;
  justify-content: center;
}
</style>