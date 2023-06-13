<script setup>
import MainHeader from "./main-header.vue";
import MainFooter from "./main-footer.vue";
import { ref, onMounted, computed } from "vue";
import RoxtawLogo from "../assets/svgs/roxtaw-logo.vue";

/**REACTIVE STATES */
const splashOpacity = ref(1);
const splashLogoFillOpacity = ref("rgb(0 0 0 / 0)");

/**COMPUTED PROPERTIES*/
const splashStyle = computed(() => {
  return {
    opacity: `${splashOpacity.value}`,
    transition: `opacity 0.5s`,
  };
});
const splashLogoStyle = computed(() => {
  return {
    fill: "rgb(0 0 0 / 1)",
    transition: `fill 5s`,
  };
});

/**FUNCTIONS */
function noScroll() {
  document.body.classList.add("no-scroll");
  setTimeout(() => {
    document.body.classList.remove("no-scroll");
    splashOpacity.value = 0;
  }, 3000);
}

/**HOOKS*/
onMounted(() => {
  noScroll();
});
</script>
<template>
  <div
    id="splash-screen"
    class="fixed flex items-center top-0 right-0 bottom-0 left-0 w-full overflow-hidden pointer-events-none bg-[#f7f8f2] z-50 max-h-full"
    :style="splashStyle"
  >
    <div id="brand-logo" class="relative w-[200px] mx-auto align-middle">
      <roxtaw-logo class="splashLogo stroke-black stroke-1"></roxtaw-logo>
    </div>
  </div>
  <main-header></main-header>

  <div id="main-content" class="relative">
    <slot name="mainContent"></slot>
  </div>

  <main-footer></main-footer>
</template>

<style scoped>
.splashLogo {
  fill: rgb(0 0 0 / 0);
  animation: splashLogoFadeIn 2s ease-out 1s forwards;
}

@keyframes splashLogoFadeIn {
  to {
    fill: rgb(0 0 0 / 1);
  }
}
</style>
