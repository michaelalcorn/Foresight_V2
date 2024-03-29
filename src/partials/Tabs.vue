<template>
  <section>
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="py-12 md:py-20 border-t border-gray-800">
        <!-- Section header -->
        <div class="max-w-3xl mx-auto text-center pb-12" data-aos-id-tabs>
          <h2 class="h2 mb-4" data-aos="fade-up" data-aos-anchor="[data-aos-id-tabs]">
            Codify, Capture, and Capitalize
          </h2>
        </div>

        <!-- Section content -->
        <div>
          <!-- Tabs buttons -->
          <div
            class="flex flex-wrap justify-center -m-2"
            data-aos="fade-up"
            data-aos-delay="400"
            data-aos-anchor="[data-aos-id-tabs]"
          >
            <button
              :class="{ 'opacity-50': tab !== '1' }"
              class="flex items-center font-medium py-2 px-4 m-2 bg-gray-400 rounded-full group transition duration-500"
              @click="tab = '1'"
            >
              <svg
                class="w-4 h-4 fill-current text-purple-600 mr-2"
                viewBox="0 0 16 16"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M13.5 5.5c-.311.001-.62.061-.909.177l-2.268-2.268c.116-.29.176-.598.177-.909a2.5 2.5 0 00-5 0c.001.311.061.62.177.909L3.409 5.677A2.473 2.473 0 002.5 5.5a2.5 2.5 0 000 5c.311-.001.62-.061.909-.177l2.268 2.268c-.116.29-.176.598-.177.909a2.5 2.5 0 105 0 2.473 2.473 0 00-.177-.909l2.268-2.268c.29.116.598.176.909.177a2.5 2.5 0 100-5zM8 11c-.311.001-.62.061-.909.177L4.823 8.909a2.423 2.423 0 000-1.818l2.268-2.268a2.423 2.423 0 001.818 0l2.268 2.268a2.423 2.423 0 000 1.818l-2.268 2.268A2.473 2.473 0 008 11z"
                />
              </svg>
              <span
                class="text-gray-800 group-hover:text-gray-900 transition-colors duration-150 ease-in-out"
                >Codify</span
              >
            </button>
            <button
              :class="{ 'opacity-50': tab !== '2' }"
              class="flex items-center font-medium py-2 px-4 m-2 bg-gray-400 rounded-full group transition duration-500"
              @click="tab = '2'"
            >
              <svg
                class="w-4 h-4 fill-current text-purple-600 mr-2"
                viewBox="0 0 16 16"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M9.043 6.293S9.79 1.905 6.745 0A5.37 5.37 0 014.72 3.887C3.42 5.03.974 7.6 1 10.34A6.285 6.285 0 004.451 16a3.984 3.984 0 011.394-2.755 3.253 3.253 0 001.246-2.185 5.856 5.856 0 013.1 4.881v.013a5.883 5.883 0 003.428-5.106c.216-2.574-1.194-6.074-2.445-7.218a6.793 6.793 0 01-2.13 2.663z"
                />
              </svg>
              <span
                class="text-gray-800 group-hover:text-gray-900 transition-colors duration-150 ease-in-out"
                >Capture</span
              >
            </button>
            <button
              :class="{ 'opacity-50': tab !== '3' }"
              class="flex items-center font-medium py-2 px-4 m-2 bg-gray-400 rounded-full group transition duration-500"
              @click="tab = '3'"
            >
              <svg
                class="w-4 h-4 fill-current text-purple-600 mr-2"
                viewBox="0 0 16 16"
                xmlns="http://www.w3.org/2000/svg"
              >
                <path
                  d="M8 0C3.6 0 0 3.6 0 8s3.6 8 8 8 8-3.6 8-8-3.6-8-8-8zm0 10c-1.1 0-2-.9-2-2 0-.2 0-.3.1-.5L3.6 5 5 3.6l2.5 2.5c.2-.1.3-.1.5-.1 1.1 0 2 .9 2 2s-.9 2-2 2z"
                />
              </svg>
              <span
                class="text-gray-800 group-hover:text-gray-900 transition-colors duration-150 ease-in-out"
                >Capitalize</span
              >
            </button>
          </div>

          <!-- Tabs items -->
          <div class="relative flex flex-col mt-16 transform" data-aos="fade-up">
            <!-- Item 1 -->
            <transition
              enter-active-class="transition ease-in-out duration-500 transform order-first"
              enter-from-class="opacity-0 scale-98"
              enter-to-class="opacity-100 scale-100"
              leave-active-class="transition ease-out duration-300 transform absolute"
              leave-from-class="opacity-100 scale-100"
              leave-to-class="opacity-0 scale-98"
            >
              <div class="w-full" v-show="tab === '1'">
                <article class="relative max-w-md mx-auto md:max-w-none">
                  <figure class="md:absolute md:inset-y-0 md:right-0 md:w-2/5">
                    <img
                      class="transform scale-125 m-full h-full object-contain"
                      src="../../assets/images/Codify.png"
                      width="400"
                      height="200"
                      alt="Tabs 01"
                    />
                  </figure>
                  <div
                    class="relative bg-gray-400 py-8 md:py-16 px-6 md:pr-16 md:max-w-lg lg:max-w-xl"
                  >
                    <h4 class="h4 mb-2">Codify</h4>
                    <p class="text-lg text-gray-800">
                      Turn everyone into an SME. Our structured data-driven framework
                      codifies the business needs of your buyers and end markets and maps
                      them to the capabilities of your solution.
                    </p>
                    <a
                      class="btn-sm text-white bg-purple-600 hover:bg-purple-700 mt-6"
                      href="#0"
                    >
                      <span class="text-sm">Learn more</span>
                      <svg
                        class="w-3 h-3 fill-current text-purple-400 flex-shrink-0 ml-2"
                        viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path d="M6 5H0v2h6v4l6-5-6-5z" />
                      </svg>
                    </a>
                  </div>
                </article>
              </div>
            </transition>

            <!-- Item 2 -->
            <transition
              enter-active-class="transition ease-in-out duration-500 transform order-first"
              enter-from-class="opacity-0 scale-98"
              enter-to-class="opacity-100 scale-100"
              leave-active-class="transition ease-out duration-300 transform absolute"
              leave-from-class="opacity-100 scale-100"
              leave-to-class="opacity-0 scale-98"
            >
              <div class="w-full" v-show="tab === '2'">
                <article class="relative max-w-md mx-auto md:max-w-none">
                  <figure class="md:absolute md:inset-y-0 md:left-0 md:w-1/2">
                    <img
                      class="w-full h-full object-contain"
                      src="../../assets/images/Capture.png"
                      width="400"
                      height="600"
                      alt="Capture"
                    />
                  </figure>
                  <div
                    class="relative bg-gray-400 py-8 md:py-16 px-6 md:pl-16 md:max-w-lg lg:max-w-xl md:ml-auto"
                  >
                    <h4 class="h4 mb-2">Capture</h4>
                    <p class="text-lg text-gray-800">
                      Go beyond text fields buried in CRM. Our proprietary Value
                      Assessment™ continuously captures the most important business needs
                      directly from each user
                    </p>
                    <a
                      class="btn-sm text-white bg-purple-600 hover:bg-purple-700 mt-6"
                      href="#0"
                    >
                      <span class="text-sm">Learn more</span>
                      <svg
                        class="w-3 h-3 fill-current text-purple-400 flex-shrink-0 ml-2"
                        viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path d="M6 5H0v2h6v4l6-5-6-5z" />
                      </svg>
                    </a>
                  </div>
                </article>
              </div>
            </transition>

            <!-- Item 3 -->
            <transition
              enter-active-class="transition ease-in-out duration-500 transform order-first"
              enter-from-class="opacity-0 scale-98"
              enter-to-class="opacity-100 scale-100"
              leave-active-class="transition ease-out duration-300 transform absolute"
              leave-from-class="opacity-100 scale-100"
              leave-to-class="opacity-0 scale-98"
            >
              <div class="w-full" v-show="tab === '3'">
                <article class="relative max-w-md mx-auto md:max-w-none">
                  <figure class="md:absolute md:inset-y-0 md:right-0 md:w-1/2">
                    <img
                      class="w-full h-full object-contain"
                      src="../../assets/images/Dashboard.png"
                      width="516"
                      height="387"
                      alt="Tabs 01"
                    />
                  </figure>
                  <div
                    class="relative bg-gray-400 py-8 md:py-16 px-6 md:pr-16 md:max-w-lg lg:max-w-xl"
                  >
                    <h4 class="h4 mb-2">Capitalize</h4>
                    <p class="text-lg text-gray-800">
                      Listen to real users rather than product usage. Value Intelligence™
                      benchmarks user needs so your teams can personalize revenue
                      opportunities for buyers across every end-market.
                    </p>
                    <a
                      class="btn-sm text-white bg-purple-600 hover:bg-purple-700 mt-6"
                      href="#0"
                    >
                      <span class="text-sm">Learn more</span>
                      <svg
                        class="w-3 h-3 fill-current text-purple-400 flex-shrink-0 ml-2"
                        viewBox="0 0 12 12"
                        xmlns="http://www.w3.org/2000/svg"
                      >
                        <path d="M6 5H0v2h6v4l6-5-6-5z" />
                      </svg>
                    </a>
                  </div>
                </article>
              </div>
            </transition>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Tabs",
  data: function () {
    return {
      tab: "1",
    };
  },
};
</script>
