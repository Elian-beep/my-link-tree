<template>
  <main class="content" :class="{ themeDark: isDark }">
    <div class="switchTheme">
      <button class="btn-switchTheme" @click="switchTheme">
        <i :class="`fa-solid fa-${switchThemeIcon}`"></i>
      </button>
    </div>
    <HeaderPage :isDark="isDark" />
    <BodyPage :isDark="isDark" />
    <FooterPage :isDark="isDark" />
  </main>
</template>
  
<script lang="ts">
import { defineComponent } from "vue";
import HeaderPage from "./HeaderPage.vue";
import BodyPage from "./BodyPage.vue";
import FooterPage from "./FooterPage.vue";

export default defineComponent({
  name: "ContentPage",
  components: { HeaderPage, BodyPage, FooterPage },
  emits: ["alterTheme"],
  data() {
    return {
      isDark: false,
    };
  },
  props: {
    themeIcon: {
      type: String,
      required: true,
    },
  },
  computed: {
    switchThemeIcon() {
      if (this.isDark) {
        return 'sun'
      } else {
        return 'moon';
      }
    },
  },
  methods: {
    switchTheme() {
      this.isDark = !this.isDark;
      console.log("tema dark: ", this.isDark);
      this.$emit("alterTheme", this.isDark);
    },
  },
});
</script>
  
<style scoped>
main {
  --bg: rgb(255, 255, 255);
  --shadow: rgba(255, 255, 255, 0.25);
  --color-btnTheme: rgb(26, 123, 250);
}

main.themeDark {
  --bg: rgb(22, 22, 22);
  --shadow: rgba(0, 0, 0, 0.25);
  --color-btnTheme: rgb(219, 200, 31);
}
.content {
  box-sizing: border-box;
  height: 95vh;
  width: 90vw;
  border-radius: 4px;

  background: var(--bg);
  box-shadow: -1px 5px 15px 5px var(--shadow);

  overflow-y: scroll;
}

.content::-webkit-scrollbar {
  width: 0;
}

.switchTheme {
  width: 100%;
  position: relative;
}

.btn-switchTheme {
  position: absolute;
  right: 16px;
  top: 16px;
  background: none;
  border: none;
  cursor: pointer;
}
.btn-switchTheme i{
  color: var(--color-btnTheme);
  font-size: 18pt;
  transition: background-color 0.3s, transform 0.3s ease-in;
}

@media screen and (min-width: 500px) {
  .content {
    height: 95vh;
    width: 400px;
  }
}
</style>