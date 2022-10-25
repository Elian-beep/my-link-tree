<template>
  <div>
    <ButtonLink />
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
  