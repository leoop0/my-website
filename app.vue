<script setup>
const nuxtApp = useNuxtApp();

nuxtApp.hook("page:finish", () => {
  window.scrollTo(0, 0);
});
</script>

<template>
  <transition name="home" mode="out-in">
    <div>
      <!-- <div
      :class="[displayTransition ? 'transition-display transition' : 'transition-hide transition']"
    ></div> -->
      <div :class="[displayLoader ? 'loader-display loader' : 'loader-hide loader']">
        <img src="/img/Logo.svg" alt="Logo" />
      </div>
      <Header />

      <NuxtPage></NuxtPage>

      <Cta />
    </div>
  </transition>
</template>

<script>
export default {
  data() {
    return {
      displayLoader: true,
      displayTransition: false,
    };
  },
  watch: {
    $route(to, from) {
      this.displayTransition = true;
      setTimeout(() => {
        this.displayTransition = false;
      }, 500);
    },
  },
  transition: {
    name: "home",
    mode: "out-in",
  },
  created() {
    setTimeout(() => (this.displayLoader = false), 1500);
  },
};
</script>

<style lang="scss">
// Fonts
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&family=Syne:wght@400;500;600;700&display=swap");

// Variables
:root {
  --beige: #f7f2ef;
  --blue: #09244b;
}

* {
  padding: 0;
  margin: 0;
  box-sizing: border-box;
  font-family: "Inter";
  // scroll-behavior: smooth;
}

body {
  background: var(--beige);
}

.home-enter-active,
.home-leave-active {
  transition: opacity 0.5s;
}
.home-enter,
.home-leave-active {
  opacity: 0;
}

// Global Classes

.syne {
  font-family: "Syne";
}

.wrapper {
  width: 100%;
  display: flex;
  justify-content: center;
  .container {
    max-width: 1500px;
    width: 93%;
  }
}

.btn {
  transition: all 0.3s;
  background: var(--blue);
  color: var(--beige);
  border-radius: 50px;
  padding: 14px 30px;
  border: solid 2px var(--blue);
  font-weight: 600;
  text-decoration: none;
  display: block;
  width: fit-content;
  &:hover {
    background: #103160;
    transform: scale(1.05) rotate(-5deg);
  }
  &.secondary {
    background: var(--beige);
    color: var(--blue);
  }
}

.loader {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 1000;
  background-color: var(--beige);
  transition: all 0.3s ease-in-out;
  img {
    width: 200px;
    animation: rotation 1.5s infinite linear;
  }
}

.loader-hide {
  transform: translateY(-100vh);
}

.loader-display {
  transform: translateY(0vh);
}

.transition {
  width: 100vw;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
  background-color: var(--beige);
  transition: all 0.3s ease-in-out;
}

.transition-display {
  transform: translateX(0vw);
}

.transition-hide {
  transform: translateX(-100vw);
}

@keyframes rotation {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(359deg);
  }
}
</style>
