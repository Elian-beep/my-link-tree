<template>
  <div class="container" :class="{ themeDark: isDark }">
    <ContentPage @alterTheme="switchTheme"> </ContentPage>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import ContentPage from "./ContentPage.vue";

export default defineComponent({
  name: "ContainerPage",
  components: { ContentPage },
  data() {
    return {
      isDark: false,
    };
  },
  methods: {
    switchTheme(isDark: boolean) {
      this.isDark = isDark;
      console.log(`Tema no container: ${this.isDark}`);
    },
  },
});
</script>

<style scoped>
div {
  --bg: #e4e3e3;
}

div.themeDark {
  --bg: #636363;
}
.container {
  height: 100vh;
  max-width: 100vw;

  display: flex;
  align-items: center;
  justify-content: center;
}

.container {
  background: var(--bg) url("https://static.tumblr.com/03fbbc566b081016810402488936fbae/pqpk3dn/MRSmlzpj3/tumblr_static_bg3.png") repeat 0 0;
  -webkit-animation: 10s linear 0s normal none infinite animate;
  -moz-animation: 10s linear 0s normal none infinite animate;
  -ms-animation: 10s linear 0s normal none infinite animate;
  -o-animation: 10s linear 0s normal none infinite animate;
  animation: 10s linear 0s normal none infinite animate;
}

@-webkit-keyframes animate {
  from {
    background-position: 0 0;
  }
  to {
    background-position: 500px 0;
  }
}

@-moz-keyframes animate {
  from {
    background-position: 0 0;
  }
  to {
    background-position: 500px 0;
  }
}

@-ms-keyframes animate {
  from {
    background-position: 0 0;
  }
  to {
    background-position: 500px 0;
  }
}

@-o-keyframes animate {
  from {
    background-position: 0 0;
  }
  to {
    background-position: 500px 0;
  }
}

@keyframes animate {
  from {
    background-position: 0 0;
  }
  to {
    background-position: 500px 0;
  }
}
</style>