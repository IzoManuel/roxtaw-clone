<script setup>
import RoxtawLogo from "../assets/svgs/roxtaw-logo.vue";
</script>

<template>
  <section id="footer">
    <div
      id="footer-content"
      class="relative wp:lg:mt-[150px] wp:md:mt-[90px] bg-[#31366e] text-[14px] leading-[22px] text-[#fff] py-[100px]"
    >
      <div
        id="footer-container"
        class="max-w-[1170px] mx-auto px-[15px] w-full"
      >
        <div id="footer-grid" class="flex flex-col lg:flex-row">
          <div
            id="col-left"
            class="lg:w-5/12 p-[15px] flex flex-col justify-between"
          >
            <div id="footer-branding">
              <div id="footer-logo" class="w-[120px] cursor-pointer">
                <roxtaw-logo class="stroke-white fill-white"></roxtaw-logo>
              </div>
              <div id="footer-logo-text" class="mt-[18px]">
                <p class="text-[14px] leading-[22px]">
                  We Invest & Scale DTC Brands
                </p>
              </div>
            </div>
            <div id="footer-copyright">
              <p>Copyright © 2020 Roxtaw.</p>
            </div>
          </div>
          <div id="col-left" class="lg:w-7/12 p-[15px]">
            <div id="footer-infos" class="grid md:grid-cols-2 grid-cols-1">
              <div
                :key="index"
                v-for="(item, index) in [
                  {
                    text: 'Tell us about your startup',
                    subtext: 'Lets talk about it',
                  },
                  {
                    text: 'Call us',
                    subtext: '+972-502288880',
                  },
                  {
                    text: 'Become an Affiliate',
                    subtext: 'Affiliate@roxtaw.com',
                  },
                  {
                    text: 'Become an Investor',
                    subtext: 'Investor@roxtaw.com',
                  },
                  {
                    text: 'Head office',
                    subtext: 'Dizengoff198, Tel-Aviv, Israel',
                  },
                ]"
                id="footer-info-row"
                class="w pb-[35px] last:pb-0"
              >
                <div
                  id="footer-info-talk"
                  class="mx-[28px] pt-[17px] border-t-[1px] border-t-[#ffffff33]"
                >
                  <div id="footer-info-text" class="mb-[5px]">
                    <h4 class="text-[14px] leading-[22px] opacity-30">
                      {{ item.text }}
                    </h4>
                  </div>
                  <div
                    id="footer-info-text"
                    class="text-[20px] leading-[30px] font-domine"
                  >
                    <span class="transition hover:text-[#ff7549] cursor-pointer">{{ item.subtext }}</span>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>
