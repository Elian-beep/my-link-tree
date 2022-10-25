<template>
  <div class="content">
    <HeaderPage />

  </div>
</template>
  
  <script lang="ts">
import { defineComponent } from "vue";
import HeaderPage from './HeaderPage.vue';

export default defineComponent({
  name: "ContentPage",
  components: { HeaderPage }
});
</script>
  
<style scoped>
.content{
    height: 95vh;
    width: 90vw;
    border-radius: 4px;

    background: rgb(246, 246, 246);
    box-shadow: -1px 5px 15px 5px rgba(0,0,0,0.55);
}

@media screen and (min-width: 500px) {
    .content{
        height: 95vh;
        width: 400px;

    }
}
</style>