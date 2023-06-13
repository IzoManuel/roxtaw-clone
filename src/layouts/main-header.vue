<script setup>
import RoxtawLogo from "../assets/svgs/roxtaw-logo.vue";
import { ref, onMounted, computed } from "vue";

/**REACTIVE STATE*/
const navTranslateY = ref(0);
const logoTextRef = ref({});

/**COMPUTED PROPERTIES */
const navStyle = computed(() => {
  return {
    right:`${navTranslateY.value}%`,
    transition: `right 0.3s`,
  };
});

const logoNavStyle = computed(() => {
  return {
    left:`${navTranslateY.value}%`,
    transition: `left 0.3s`,
  };
});

/** FUNCTIONS */
function updateNavPosition() {
  const scrollPosition = document.documentElement.scrollTop
  if (scrollPosition === 0) {
    navTranslateY.value = 0;
  } else {
    navTranslateY.value = -100;
  }
}

/**HOOK */
onMounted(() => {
  window.addEventListener("scroll", updateNavPosition);
});
</script>
<template>
  <div id="navbar">
    <nav id="navbar-strip" class="fixed flex-nowrap right-0 left-0 z-50">
      <div id="navbar-container" class="p-[40px]">
        <div id="navbar-grid" class="font-poppins flex items-center justify-between">
          <div id="col-left" class="flex items-center">
            <div id="navbar-logo" class="w-[119px] h-[24px]">
              <roxtaw-logo class="stroke-black fill-black"></roxtaw-logo>
            </div>
            <div id="navbar-title" class="overflow-hidden" >
                <span class="relative ml-[10px] border-l-[1px] pl-[10px] text-[12px] font-bold" :style="logoNavStyle">We Invest & Scale DTC Brands</span>
            </div>
          </div>
          <div id="col-right" class="">
            <div id="navbar-navs" class="inline-block pr-[50px]">
              <div
                :key="index"
                v-for="(nav, index) in [
                  'Hello',
                  'How it works',
                  'Why choose us',
                  'Portfolio',
                  'Testimonial',
                ]"
                class="inline-block overflow-hidden align-bottom"
              >
                <span class="px-[25px] relative" :style="navStyle">{{ nav }}</span>
              </div>
            </div>
            <div id="navbar-action" class="inline-block">
                <button class="rounded-full text-white bg-[#ff7549] font-[600] shadow-lg shadow-[#ff7549] w-[164px] h-[66px]">
                    Get in touch
                </button>
            </div>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>
