<template>
  <footer>
    <i :class="nameIcon" :style="style"></i>
  </footer>
</template>
    
<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "IconTec",
  props: {
    nameIcon: {
        type: String,
        required: true
    },
    fontColor: {
        type: String,
        required: false
    }
  },
  computed: {
    style(){
        return 'color: ' + this.fontColor;
    }
  }
});
</script>
    
<style scoped>
i{
    font-size: 16pt;
}
</style>
    