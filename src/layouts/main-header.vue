<script setup>
import RoxtawLogo from "../assets/svgs/roxtaw-logo.vue";
import { ref, onMounted, computed } from "vue";
import ButtonIcon from "../assets/svgs/btn-icon.vue";
import MenuBar from "../components/menu-bar.vue";

/**REACTIVE STATE*/
const navTranslateY = ref(0);
const logoTextRef = ref({});
const actionButton = ref({
  width: 164,
});
const abw = ref(164);

/**COMPUTED PROPERTIES */
const navStyle = computed(() => {
  return {
    right: `${navTranslateY.value}%`,
    transition: `right 0.3s`,
  };
});

const logoNavStyle = computed(() => {
  return {
    left: `${navTranslateY.value}%`,
    transition: `left 0.3s`,
  };
});

const buttonStyle = computed(() => {
  return {
    width: `${abw.value}px`,
    //transition: `width 0.3s`,
  };
});
/** FUNCTIONS */
function updateNavPosition() {
  const scrollPosition = document.documentElement.scrollTop;
  if (scrollPosition === 0) {
    navTranslateY.value = 0;
    actionButton.width = 164;
  } else {
    navTranslateY.value = -100;
    actionButton.width = 66;
  }
  console.log(`ABV:${actionButton.width}`);
}

/**HOOK */
onMounted(() => {
  window.addEventListener("scroll", updateNavPosition);
});
</script>
<template>
  <div id="navbar">
    <nav id="navbar-strip" class="fixed flex-nowrap right-0 left-0 z-40">
      <div id="navbar-container" class="p-[40px]">
        <div
          id="navbar-grid"
          class="font-poppins flex items-center justify-between"
        >
          <div id="col-left" class="flex items-center">
            <div id="navbar-logo" class="w-[119px] h-[24px] cursor-pointer">
              <roxtaw-logo class="stroke-black fill-black"></roxtaw-logo>
            </div>
            <div id="navbar-title" class="hidden xl:block overflow-hidden">
              <span
                class="relative ml-[10px] border-l-[1px] pl-[10px] text-[12px] font-bold"
                :style="logoNavStyle"
                >We Invest & Scale DTC Brands</span
              >
            </div>
          </div>
          <div id="col-right" class="">
            <div id="navbar-navs" class="inline-block lg:pr-[50px]">
              <!-- <div
                class="inline-block overflow-hidden align-bottom cursor-pointer"
              >
                <div class="px-[25px] relative group overflow-hidden" :style="navStyle">
                  <div id="front" class="relative">
                    <span
                      class="relative group-hover:bottom-[10px]"
                      style="transition:bottom 10s;"
                      >H</span
                    >
                    <span>e</span>
                    <span>l</span>
                    <span>l</span>
                    <span>o</span>
                  </div>
                  <div id="back" class="absolute text-[#ff7549]">
                    <span
                      class="relative transition group-hover:bottom-[10px] duration-1000"
                      >H</span
                    >
                    <span>e</span>
                    <span>l</span>
                    <span>l</span>
                    <span>o</span>
                  </div>
                </div>
              </div> -->
              <div
                :key="index"
                v-for="(nav, index) in [
                  'Hello',
                  'How it works',
                  'Why choose us',
                  'Portfolio',
                  'Testimonial',
                ]"
                class="hidden xl:inline-block overflow-hidden align-bottom transition hover:text-[#ff7549] cursor-pointer"
              >
                <span class="px-[25px] relative" :style="navStyle">{{
                  nav
                }}</span>
              </div>
              <menu-bar class="xl:hidden"></menu-bar>
            </div>
            <div id="navbar-action" class="hidden xl:inline-block">
              <button
                class="relative overflow-hidden rounded-full text-white bg-[#ff7549] font-[600] shadow-lg shadow-[#ff7549] w-[164px] h-[66px]"
              >
                <span class="relative">Get in touch</span>
                <!-- <span
                  id="btn-icon"
                  class="absolute left-0 top-0 w-[68px] h-[68px] text-white"
                >
                  <button-icon class="stroke-[#fff]" style="transform: rotate(-90deg)"></button-icon>
                </span> -->
              </button>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>
