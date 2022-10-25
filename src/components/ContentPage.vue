<template>
  <div class="content">
    <ImageProfile />

  </div>
</template>
  
  <script lang="ts">
import { defineComponent } from "vue";
import ImageProfile from "./ImageProfile.vue";

export default defineComponent({
  name: "ContentPage",
  components: { ImageProfile }
});
</script>
  
<style scoped>
.content{
    /* border: 1px solid #000; */
    height: 100vh;
    width: 100vw;

    background: rgb(246, 246, 246);
}

@media screen and (min-width: 500px) {
    .content{
        height: 95vh;
        width: 400px;

        border-radius: 4px;
    }
}
</style>