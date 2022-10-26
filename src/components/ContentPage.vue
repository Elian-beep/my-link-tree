<template>
  <div class="content">
    <HeaderPage />
    <BodyPage />
  </div>
</template>
  
<script lang="ts">
import { defineComponent } from "vue";
import HeaderPage from "./HeaderPage.vue";
import BodyPage from "./BodyPage.vue";

export default defineComponent({
  name: "ContentPage",
  components: { HeaderPage, BodyPage },
});
</script>
  
<style scoped>
.content {
  height: 95vh;
  width: 90vw;
  border-radius: 4px;

  background: rgb(246, 246, 246);
  box-shadow: -1px 5px 15px 5px rgba(0, 0, 0, 0.55);

  overflow-y: scroll;
}

.content::-webkit-scrollbar {
  width: 5px;
  border-radius: 10px;
  background-color: #1c1c1c;
}

.content::-webkit-scrollbar-thumb {
  border-radius: 10px;
  background-color: #363636;
}

@media screen and (min-width: 500px) {
  .content {
    height: 95vh;
    width: 400px;
  }
}
</style>