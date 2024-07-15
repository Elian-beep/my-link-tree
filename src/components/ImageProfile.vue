<template>
  <div>
    <img
      class="image-profile"
      src="@/assets/Perfil-Elian.png"
      alt="Avatar Elian"
    />
  </div>
</template>
    
<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ImageProfile",
});
</script>
    
<style scoped>

div{
    margin-top: 8px;
    display: flex;
}
.image-profile {
  height: 153px;
  width: 166;
  margin: 0px auto;
  border-radius: 50%;
}
</style>