<script setup>
import BaseLayout from "../layouts/base-layout.vue";
import ButtonIcon from "../assets/svgs/btn-icon.vue";
import Parallaxy from "@lucien144/vue3-parallaxy";
import HeroCloud from "../assets/svgs/hero-cloud.vue";
import Chevron from "../assets/svgs/chevron.vue";
import RoxtawLogo from "../assets/svgs/roxtaw-logo.vue";
</script>

<template>
  <base-layout>
    <template #mainContent>
      <section id="hero">
        <div
          id="hero-content"
          class="relative overflow-hidden h-screen flex items-center bg-white pb-[100px]"
        >
          <div
            id="hero-sun"
            class="absolute right-[14.30556%] top-[200px] w-[492px] h-[492px] bg-[#fff5dd] block rounded-[50%]"
          ></div>
          <div id="hero-cloud" class="absolute bottom-[100px] left-0 w-[60%]">
            <img src="../assets/svgs/hero-cloud.svg" class="align-middle" />
          </div>
          <Parallaxy
            class="absolute bottom-[85px] left-0 w-full"
            :speed="200"
            :direction="'opposite'"
          >
            <div id="hero-woods">
              <img src="../assets/images/hero-woods.png" class="w-full" />
            </div>
          </Parallaxy>
          <Parallaxy
            class="absolute bottom-0 left-0 ease-out w-full overflow-hidden"
            :speed="200"
            :direction="'opposite'"
          >
            <div id="hero-bg" class="">
              <img
                src="../assets/images/climber.png"
                class="w-full object-fit"
              />
            </div>
          </Parallaxy>
          <div id="hero-mountain" class="absolute -bottom-[5px] left-0 w-full">
            <img
              src="../assets/images/mountain.png"
              class="w-full object-fit"
            />
          </div>
          <div
            id="hero-container"
            class="max-w-[1170px] mx-auto px-[15px] w-full z-10"
          >
            <div id="hero-text">
              <div id="hero-header">
                <h2
                  class="font-domine font-[700] text-[48px] leading-[62px] text-[#30376a] max-w-[530px]"
                >
                  Ready to be the next
                  <span class="text-[#00aca2]">$1 Billion </span> DTC brand?
                </h2>
              </div>
              <div
                id="hero-description"
                class="mt-[1em] mb-[1.5em] max-w-[500px]"
              >
                <p>
                  We invest in and scale your DTC brands exponentially to that
                  10-figure milestone.
                </p>
              </div>
            </div>
            <div id="hero-action">
              <button class="flex items-center">
                <span
                  id="btn-icon"
                  class="relative w-[68px] h-[68px] border-2 border-[#ff7549] text-[#ff7549] hover:text-white rounded-[50%] before:absolute hover:before:bg-[#ff7549] top-0 left-0 before:w-full before:h-full before:block before:rounded-[50%]"
                >
                  <button-icon class="stroke-[#ff7549]"></button-icon>
                </span>
                <span id="button-text" class="ml-[15px] font-semibold"
                  >Explore how it works?</span
                >
              </button>
            </div>
          </div>
        </div>
      </section>
      <section id="how" class="z-50">
        <div
          id="how-content"
          class="bg-[#101a56] pt-[110px] pb-[60px] -mt-[4px] -mb-[5px]"
        >
          <div
            id="how-container"
            class="max-w-[1170px] mx-auto px-[15px] w-full"
          >
            <div id="how-text" class="mx-auto text-center">
              <div id="how-heading">
                <h1
                  class="text-[16px] leaading-[24px] text-[#00aca2] font-[600] mb-[10px]"
                >
                  How it works
                </h1>
              </div>
              <div
                id="how-subheading"
                class="max-w-[800px] mx-auto text-white font-domine text-[48px] leading-[62px]"
              >
                <h1>
                  What Happens When We Become Your
                  <span
                    class="text-[#ffffff33] line-through decoration-[#00aca2]"
                    >Investor</span
                  >
                  Partner
                </h1>
              </div>
            </div>
          </div>
          <div
            id="how-slides-content"
            class="cursor-grab mt-[140px] overflow-x-hidden relative w-scren"
          >
            <div
              id="how-counter"
              class="font-[700] text-[200px] leading-[1] h-[170px] overflow-hidden flex items-center text-[#ffffff0d] font-domine absolute top-[0] left-[50%] -translate-x-[50%] pr-[120px]"
            >
              <span class="static block">0</span>
              <span class="absolute left-[135px] block">1</span>
              <span class="absolute left-[135px] hidden">2</span>
            </div>
            <div id="how-slides" class="flex">
              <div id="how-slide-item" class="flex w-[80%] grow-0 shrink-0">
                <div id="how-fig" class="w-[757px]">
                  <img
                    src="../assets/images/how-plant.png"
                    class="w-[600px] mx-auto"
                  />
                </div>

                <div
                  id="how-text"
                  class="text-[#ffffffcc] pt-[80px] relative w-[37%]"
                >
                  <div id="how-header">
                    <h1
                      class="text-[#00aca2] text-[16px] font-[600] leading-[24px] mb-[5px]"
                    >
                      Invest
                    </h1>
                  </div>
                  <div id="how-subheader" class="">
                    <h1
                      class="text-[#fff] text-[32px] leading-[42px] font-[700] font-domine"
                    >
                      Secured the Required Capital
                    </h1>
                  </div>
                  <div id="how-description" class="mt-[1.5em]">
                    <p class="mb-[1.5em]">
                      Unlike traditional holding companies who only see
                      E-commerce brands as dollars and try to get as much equity
                      as possible, we invest in your startup in such a way that
                      allows you to keep growing.
                    </p>
                    <p class="mb-[1.5em]">
                      We've bootstrapped zero to hero so many times that we know
                      your numbers better than you.
                    </p>
                  </div>
                </div>
              </div>
              <div id="how-slide-item" class="flex w-[80%] grow-0 shrink-0">
                <div id="how-fig" class="w-[757px]">
                  <img
                    src="../assets/images/trophy.png"
                    class="w-[600px] mx-auto"
                  />
                </div>

                <div
                  id="how-text"
                  class="text-[#ffffffcc] pt-[80px] relative w-[37%]"
                >
                  <div id="how-header">
                    <h1
                      class="text-[#00aca2] text-[16px] font-[600] leading-[24px] mb-[5px]"
                    >
                      Scale
                    </h1>
                  </div>
                  <div id="how-subheader" class="">
                    <h1
                      class="text-[#fff] text-[32px] leading-[42px] font-[700] font-domine"
                    >
                      Get From Zero to 10-Fig Hero
                    </h1>
                  </div>
                  <div id="how-description" class="mt-[1.5em]">
                    <p class="">
                      At this point, after you have the cash, usually you'll be
                      on your own pulling hair and trying to figure the DTC
                      game. However, when you're funded by us, not only you get
                      money (which is awesome) but you also join our family and
                      we help you step by step in growing and scaling your
                      business into 8, 9, or 10-fig E-commerce brand.
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section id="why">
        <div id="why-content" class="">
          <div
            id="expertise"
            class="relative overflow-hidden pb-[500px] pt-[350px] before:absolute before:left-0 before:h-full before:w-full before:top-0 2xl:py-[550px]"
            style=""
          >
            <div id="expertise-title" class="">
              <Parallaxy
                :axis="'x'"
                :speed="800"
                class="absolute top-[50px] z-10"
              >
                <h2
                  class="text-[160px] leading-[180px] opacity-[0.2] whitespace-nowrap font-domine"
                  style="
                    -webkit-text-stroke: 1.5px #fff;
                    -webkit-text-fill-color: transparent;
                  "
                >
                  Why it's better together
                </h2>
              </Parallaxy>
            </div>
            <Parallaxy
              :speed="200"
              :direction="'opposite'"
              class="absolute left-0 w-full wpb-[17.01389%] bottom-[10.7vw]"
            >
              <div id="expertise-moutain" class="">
                <img src="../assets/svgs/exp-mountain.svg" class="w-full" />
              </div>
            </Parallaxy>
            <div
              id="expertise-mid-ground"
              class="absolute left-0 bottom-0 w-full h-0 pb-[56.77083%]"
            >
              <img
                src="../assets/images/exp-mid-ground.png"
                class="w-full object-fit z-20"
              />
            </div>
            <Parallaxy
              :speed="100"
              class="absolute right-0 w-full -bottom-[50px] after:w-full after:absolute after:h-[300px] after:bg-[#0e1b56] after:block after:top-[100%] after:left-0 after:-mt-[10px]"
            >
              <div id="expertise-fore-ground" class="">
                <img src="../assets/svgs/exp-fore-ground.svg" />
              </div>
            </Parallaxy>
            <div id="expertise-clouds" class="w-full">
              <img
                src="../assets/images/cloud1.png"
                class="floating-cloud absolute w-[200px]"
              />
              <img
                src="../assets/images/cloud2.png"
                class="floating-cloud absolute top-[600px] w-[100px]"
              />
              <img
                src="../assets/images/cloud1.png"
                class="floating-cloud absolute w-[350px] top-[350px]"
              />
              <img
                src="../assets/images/cloud1.png"
                class="floating-cloud absolute w-[250px] top-[700px]"
              />
              <img
                src="../assets/images/cloud1.png"
                class="floating-cloud absolute w-[300px] top-[50px]"
              />
            </div>
            <div
              id="expertise-container"
              class="relative max-w-[1170px] mx-auto px-[15px] w-full"
            >
              <div id="expertise-content" class="text-[#fff]">
                <div id="expertise-text">
                  <div id="expertise-header" class="max-w-[545px]">
                    <h1
                      class="text-[32px] leading-[42px] font-domine font-[700]"
                    >
                      It's ok, we've all been there. We know exactly what it
                      takes to scale your E-commerce brand.
                    </h1>
                  </div>
                  <div id="expertise-subheader" class="mt-[30px] mb-[10px]">
                    <h2
                      class="text-[20px] leading-[30px] font-[700] font-domine"
                    >
                      OUR EXPERTISE:
                    </h2>
                  </div>
                </div>
                <div id="expertise-list" class="flex">
                  <div id="col-left">
                    <div
                      :key="index"
                      v-for="(item, index) in [
                        'Paid advertising',
                        'SEO',
                        'Sourcing',
                        'Content marketing',
                        'Product design',
                        'Inspection',
                      ]"
                      id="expertise-list-item"
                      class="relative pl-[36px] leading-[40px]"
                    >
                      <span>{{ item }}</span>
                    </div>
                  </div>
                  <div id="col-right" class="ml-[115px]">
                    <div
                      :key="index"
                      v-for="(item, index) in [
                        'Logistics',
                        'AI',
                        'PR',
                        'Funnel',
                        'Mechanical Engineering',
                      ]"
                      id="expertise-list-item"
                      class="relative pl-[36px] leading-[40px]"
                    >
                      <span>{{ item }}</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div id="why-us"
            class="relative -top-[1px] text-[#fff] pt-[140px] bg-[#0e1b56]"
          >
            <div id="why-us-container"
              class="relative max-w-[1170px] mx-auto px-[15px] w-full"
            >
              <div id="why-us-text">
                <div
                  id="why-us-description"
                  class="lg:px-[100px] text-center max-w-full mx-auto"
                >
                  <h1
                    class="font-[700] text-center text-[30px] sm:text-[48px] leading-[62px] font-domine whitespace-normal"
                  >
                    Isn't it much better for your business to get funded today
                    and reach <span class="text-[#00aca2]">$100M</span> or
                    <span class="text-[#00aca2]">$1B</span> in evaluation within
                    5 years or less, instead of wasting 25 years of trial and
                    errors, all by yourself?
                  </h1>
                </div>
              </div>
            </div>
            <div id="why-choose-bg"
              class="mt-[100px] relative bg-[#0f1b56] pb-[39.0625%]"
            >
              <img
                src="../assets/images/why-lab.jpg"
                class="w-full object-cover absolute"
              />
              <div
                id="astronaut"
                class="absolute left-[45%] bottom-[16.07vw] w-[10.11905%] opacity-90"
              >
                <img
                  src="../assets/images/astronaut.png"
                  class="astronaut-dance w-[200px]"
                />
              </div>
              <div
                id="why-choose-bubbles"
                class="w-[14.88095%] h-[300px] bottom-[11.9vw] absolute -translate-x-[50%] left-[45%] inline-block"
              >
                <span
                  id="bubble"
                  class="floating-bubble h-[10px] w-[10px] rounded-[50%] absolute bottom-0 left-[50%] bg-[#ffffff66]"
                ></span>
                <span
                  id="bubble"
                  class="floating-bubble -ml-[17px] bottom-[25px] h-[13px] w-[12px] rounded-[50%] absolute left-[50%] bg-[#ffffff66]"
                ></span>
                <span
                  id="bubble"
                  class="floating-bubble ml-[25px] mb-[10px] bottom-[10px] h-[10px] w-[10px] rounded-[50%] absolute left-[50%] bg-[#ffffff66]"
                ></span>
                <span
                  id="bubble"
                  class="floating-bubble -ml-[10px] h-[7px] w-[6px] bottom-[40px] rounded-[50%] absolute left-[50%] bg-[#ffffff66]"
                ></span>

                <span
                  id="bubble"
                  class="floating-bubble h-[10px] w-[10px] rounded-[50%] absolute bottom-0 left-[100%] bg-[#ffffff66]"
                ></span>
                <span
                  id="bubble"
                  class="floating-bubble -ml-[17px] bottom-[25px] h-[13px] w-[12px] rounded-[50%] absolute left-[100%] bg-[#ffffff66]"
                ></span>
                <span
                  id="bubble"
                  class="floating-bubble ml-[25px] mb-[10px] bottom-[10px] h-[10px] w-[10px] rounded-[50%] absolute left-[100%] bg-[#ffffff66]"
                ></span>
                <span
                  id="bubble"
                  class="floating-bubble -ml-[10px] h-[7px] w-[6px] bottom-[40px] rounded-[50%] absolute left-[100%] bg-[#ffffff66]"
                ></span>
              </div>
            </div>
            <div id="why-choose-footer" class="bg-[#fff] pb-[100px] -mt-[0px]">
              <div
                id="why-choose-container"
                class="max-w-[1170px] mx-auto px-[15px] w-full"
              >
                <div
                  id="grid"
                  class="grid md:grid-cols-2 grid-cols-1 -ml-[15px] -mr-[15px] relative items-center"
                >
                  <div id="left-col" class="relative p-[15px]">
                    <div id="why-choose-text" class="mb-[5px] max-w-[440px]">
                      <h1
                        class="text-[48px] leading-[62px] text-[#30376a] font-domine font-[700]"
                      >
                        Let's Do Your Company a Favor and Get Funded Today!
                      </h1>
                    </div>
                  </div>
                  <div id="right-col" class="relative p-[15px]">
                    <div
                      id="why-choose-cta"
                      class="flex items-center justify-center relative w-ful h-[558px] overflow-hidden"
                    >
                      <span
                        id="why-choose-cirle"
                        class="w-full h-full bg-[#ff75490d] rounded-[50%] absolute"
                      ></span>
                      <span
                        id="why-choose-cirle"
                        class="w-[442px] h-[442px] bg-[#ff75490d] rounded-[50%] absolute"
                      ></span>
                      <span
                        id="why-choose-cirle"
                        class="w-[332px] h-[332px] bg-[#ff75490d] rounded-[50%] absolute"
                      ></span>
                      <button
                        id="why-choose-action"
                        class="w-[197px] h-[197px] bg-[#ff7549] rounded-[50%] absolute text-[#fff] font-[600]"
                      >
                        Get in touch
                      </button>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      <section
        id="portfolio"
        class="pt-[100px] pb-[130px] bg-[#30376a] text-[#fff] relative"
      >
        <div
          id="portfolio-container"
          class="max-w-[1170px] mx-auto px-[15px] w-full relative overflow-hidden"
        >
          <div id="portfolio-grid" class="flex flex-col md:flex-row">
            <div id="col-left" class="p-[15px]">
              <div id="porfolio-text" class="">
                <div id="portfolio-header" class="mb-[10px]">
                  <h1
                    class="text-[16px] leading-[24px] text-[#00aca2] font-[600]"
                  >
                    Portfolio
                  </h1>
                </div>
                <div id="portfolio-subheader" class="max-w-[460px]">
                  <h2
                    class="text-[#fff] text-[48px] leading-[62px] font-domine font-[700]"
                  >
                    Founders are nurtured, not born
                  </h2>
                </div>
                <div id="portfolio-description" class="mt-[30px] mb-[24px]">
                  <p>
                    Unlike other investors, Roxtaw does not perform
                    "fire-and-forget" investing. Rather, we provide continual
                    and practical support to help you achieve the mastery of
                    trade.
                  </p>
                </div>
                <div id="portfolio-cta" class="mt-[20px]">
                  <button class="flex items-center">
                    <span
                      id="btn-icon"
                      class="relative w-[68px] h-[68px] border-2 border-[#ff7549] text-[#ff7549] hover:text-white rounded-[50%] before:absolute hover:before:bg-[#ff7549] top-0 left-0 before:w-full before:h-full before:block before:rounded-[50%]"
                    >
                      <button-icon
                        class="stroke-[#ff7549]"
                        style="transform: rotate(-90deg)"
                      ></button-icon>
                    </span>
                    <span id="button-text" class="ml-[15px] font-semibold"
                      >Join us now</span
                    >
                  </button>
                </div>
              </div>
            </div>
            <div id="col-right" class="p-[15px]">
              <div id="portfolio-text">
                <div
                  id="portfolio-list"
                  class="flex flex-col pl-[50px] md:min-w-[350px]"
                >
                  <div
                    :key="index"
                    v-for="(item, index) in [
                      'CorePhotonics',
                      'AxumGear',
                      'Exobone',
                      'Kraftgun',
                      'Wellfryer',
                      'TryGlow',
                      'TorroBand',
                    ]"
                    id="porfolio-item"
                    :class="`relative py-[13px] pl-[27px] transition hover:text-[#ff7549] cursor-pointer before:content-['00.'] before:text-[#fff] before:opacity-30 before:text-[14px] before:absolute before:left-0 before:top-[18px]`"
                  >
                    <h3
                      class="text-[24px] leading-[42px] font-domine font-[700]"
                    >
                      {{ item }}
                    </h3>
                  </div>
                </div>
                <div id="portfoio-images"></div>
              </div>
            </div>
          </div>
        </div>
      </section>
      
      <section id="testimonial" class="pt-[185px] relative bg-[#fff]">
        <div
          id="testimonial-container"
          class="max-w-[1170px] mx-auto px-[15px] w-full"
        >
          <div id="grid" class="grid grid-cols-2">
            <div id="col-left" class="p-[15px]">
              <div id="testimonial-text">
                <div id="heading" class="mb-[10px]">
                  <h4
                    class="text-[16px] leading-[24px] text-[#00aca2] font-[600]"
                  >
                    Testimonials
                  </h4>
                </div>
                <div id="subheading" class="">
                  <h2
                    class="max-w-[410px] text-[#30376a] text-[48px] leading-[62px] font-domine font-[700]"
                  >
                    What our Founders say
                  </h2>
                </div>
              </div>
              <div
                id="testimonial-controls"
                class="flex items-center mt-[49px]"
              >
                <div
                  id="testimonial-progress"
                  class="relative h-[3px] bg-[#2525251a] w-[140px] mr-[10px]"
                >
                  <span
                    id="testimoial-progress-value"
                    class="absolute left-0 top-0 h-full bg-[#00aca2] w-full"
                  ></span>
                </div>
                <button
                  id="testimonial-control-btn"
                  class="mx-[3px] h-[30px] w-[30px] rounded-[50%]"
                >
                  <span class="inline-block w-[10px] h-[12px]">
                    <chevron></chevron>
                  </span>
                </button>
                <button
                  id="testimonial-control-btn"
                  class="mx-[3px] h-[30px] w-[30px] rounded-[50%]"
                >
                  <span class="inline-block w-[10px] h-[12px] rotate-180">
                    <chevron></chevron>
                  </span>
                </button>
              </div>
            </div>
            <div id="col-right" class="p-[15px]">
              <div
                id="testimonial-slides"
                class="relative overflow-hiden min-h-[250px]"
              >
                <div id="testimonial-item" class="wp:absolute left-0 top-0">
                  <div id="testimonial-item-name" class="mb-[5px]">
                    <h4
                      class="text-[16px] leading-[24px] text-[#30376a] font-[700]"
                    >
                      Eino Nieminen
                    </h4>
                  </div>
                  <div id="testimonial-item-pos" class="mb-[21px]">
                    <h4 class="text-[14px] leading-[22px]">GAINZBAND</h4>
                  </div>
                  <div
                    id="testimonial-item-desc"
                    class="text-[#252525] text-[20px] leading-[30px] font-domine font-[700] mb-[5px]"
                  >
                    <p>
                      The Toughest call I had to make was to pass on equity,
                    </p>
                    <p>especially when we already had some sales. But once</p>
                    <p>
                      you start scaling you realize what they mean by saying
                    </p>
                    <p>
                      "if you want to run fast,run alone. If you want to run
                      far,"
                    </p>
                    <p>run together". The partnership with ROXTAW gave me</p>
                    <p>an unfair advantage in the eCommerce game.</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
      
      <section
        id="subscribe"
        class="pt-[225px] pb-[210px] relative overflow-hidden bg-[#fff]"
      >
        <div
          id="subscribe-container"
          class="max-w-[1170px] mx-auto px-[15px] w-full"
        >
          <div id="subscribe-header" class="text-center">
            <h2
              class="text-[32px] leading-[42px] text-[#30376a] font-domine font-[700]"
            >
              Subscribe To Get Newsletter
            </h2>
          </div>
          <div
            id="subscribe-form"
            class="relative max-w-[450px] mt-[30px] mx-auto"
          >
            <div id="form-field" class="w-full z-20">
              <input
                type="email"
                placeholder="Enter your email"
                class="z-10 text-[16px] w-full h-full pt-[25px] pb-[15px] outline-none border-b-[1px] border-[#e5e5e5] text-[#252525] text-center after:w-0 mb-[1px] after:bg-[#00aca2] after:block after:absolute after:bottom-0 left-0"
              />
            </div>
            <div id="subscribe-cta" class="mt-[30px] flex justify-center">
              <button
                class="z-10 px-[33px] h-[66px] text-[#fff] bg-[#ff7549] rounded-[33px] shadow-md shadow-[#ff7549] font-[600]"
              >
                <span>Subscribe</span>
              </button>
            </div>
          </div>
        </div>
        <div id="subscribe-bg">
          <Parallaxy
            :speed="230"
            class="absolute left-0 w-full pb-[18.125%] z-10 after:w-full after:absolute after:h-[300px] after:bg-[#31366e] after:block after:top-[100%] after:left-0 after:-mt-[10px]"
          >
            <div id="subscribe-mountain">
              <img
                src="../assets/images/subscribe-mountain.png"
                class="absolute w-full h-full object-cover"
              />
            </div>
          </Parallaxy>
          <div
            id="subscribe-cloud"
            class="left-0 w-full absolute pb-[45.97222%] -bottom-[125px]"
          >
            <img
              src="../assets/svgs/footer-cloud.svg"
              class="w-full h-full object-cover absolute"
            />
          </div>
        </div>
      </section>
    </template>
  </base-layout>
</template>

<style scoped>
:root {
  --portfolio-item-index: 0;
}

div#expertise::before {
  background: radial-gradient(
    67.98% 67.98% at 30.63% 95.22%,
    #001bab 0,
    #101a56 100%
  );
}

#expertise-list-item::before {
  content: "";
  width: 18px;
  height: 18px;
  display: inline-block;
  position: absolute;
  top: 8px;
  left: 0;
  background: url("../assets/svgs/tick.svg");
}

/* #portfolio-item::before {
  content: --v
} */

.astronaut-dance {
  animation: astronautDance 7s ease-in-out infinite;
  animation-fill-mode: both;
}

@keyframes astronautDance {
  0% {
    transform: translate(0px, 0px);
  }
  50% {
    transform: translate(0px, -40px);
  }
  100% {
    transform: translate(0px, 0px);
  }
}

.floating-cloud {
  animation: floatingCloud 40s linear infinite;
}

@keyframes floatingCloud {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(600%);
  }
}

.floating-bubble {
  animation: floatingBubble 3s linear infinite;
}

@keyframes floatingBubble {
  0% {
    transform: translateY(0);
  }
  100% {
    transform: translateY(-2000%);
  }
}
</style>
