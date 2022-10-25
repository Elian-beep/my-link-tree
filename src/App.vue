<template>
  <ContainerPage></ContainerPage>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import ContainerPage from './components/ContainerPage.vue';

export default defineComponent({
  name: 'App',
  components: { ContainerPage }
});
</script>

<style>
#app {
  font-family: 'Roboto', sans-serif;
}

*{
  margin: 0;
  padding: 0;
}
</style>
