<template>
  <button :class="{ 'themeDark': isDark }" class="btnLink" @click="redirectLink">
    <i :class="icone"></i>
    <span>{{ textButton }}</span>
  </button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "ButtonLink",
  props: {
    textButton: {
      type: String,
      required: true,
    },
    inputLink: {
      type: String,
      required: true,
    },
    icone: {
      type: String,
      required: true,
    },
    isDark: {
      type: Boolean,
      required: true,
    },
  },
  methods: {
    redirectLink() {
      console.log("redirecionando para: ", this.inputLink);
      window.location.assign(this.inputLink);
    },
  },
});
</script>

<style scoped>
button{
    --color-primary: #213140;
    --color-hover: rgb(246, 246, 246);
}

button.themeDark{
    --color-primary: rgb(246, 246, 246);
    --color-hover: #213140;
}

.btnLink {
  border: 1.5px solid var(--color-primary);
  background: none;
  width: 85%;
  height: 40px;
  border-radius: 4px;

  display: flex;
  justify-content: space-around;
  align-items: center;

  color: var(--color-primary);
  font-weight: 500;
  font-size: 10.5pt;
  text-decoration: none;
  text-transform: uppercase;
  letter-spacing: 1px;

  transition: ease-in-out 0.25s;
}

.btnLink i {
  font-size: 11pt;
}

.btnLink span {
  width: 50%;
  text-align: start;
}

.btnLink:hover {
  background: var(--color-primary);
  color: var(--color-hover);
  cursor: pointer;
}
</style>