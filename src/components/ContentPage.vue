<template>
  <div class="content">
    <HeaderPage />
    <BodyPage />
    <FooterPage />
  </div>
</template>
  
<script lang="ts">
import { defineComponent } from "vue";
import HeaderPage from "./HeaderPage.vue";
import BodyPage from "./BodyPage.vue";
import FooterPage from "./FooterPage.vue";

export default defineComponent({
  name: "ContentPage",
  components: { HeaderPage, BodyPage, FooterPage },
});
</script>
  
<style scoped>
.content {
  height: 95vh;
  width: 90vw;
  border-radius: 4px;

  background: rgb(255, 255, 255);
  box-shadow: -1px 5px 15px 5px rgba(255, 255, 255, 0.25);

  overflow-y: scroll;
}

.content::-webkit-scrollbar {
  width: 0;
}

@media screen and (min-width: 500px) {
  .content {
    height: 95vh;
    width: 400px;
  }
}
</style>