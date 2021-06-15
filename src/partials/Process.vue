<template>
  <section>
    <div class="max-w-6xl mx-auto px-4 sm:px-6">
      <div class="pt-10 pb-12 md:pt-16 md:pb-20">
        <!-- Section header -->
        <div class="max-w-3xl mx-auto text-center pb-12 md:pb-20">
          <h2 class="h2 mb-4" data-aos="fade-up">
            Institutionalize Market Enterprise
          </h2>
          <p
            class="text-xl text-gray-800"
            data-aos="fade-up"
            data-aos-delay="200"
          >
            Foresight's technology turns your entire company into experts on the
            value you provide to your users, buyers, and end-markets.
          </p>
        </div>

        <!-- Items -->
        <div
          class="
            max-w-sm
            mx-auto
            grid
            gap-8
            md:grid-cols-3
            lg:gap-16
            items-start
            md:max-w-none
          "
        >
          <!-- 1st item -->
          <div class="relative flex flex-col items-center" data-aos="fade-up">
            <div
              aria-hidden="true"
              class="
                absolute
                h-1
                border-t border-dashed border-gray-700
                hidden
                md:block
              "
              style="
                width: calc(100% - 32px);
                left: calc(50% + 48px);
                top: 32px;
              "
              data-aos="fade-in"
              data-aos-delay="200"
            ></div>
            <img
              class="mx-auto"
              src="../../assets/images/revenue.png"
              width="75"
              height="75"
              alt="Revenue Teams"
            />

            <h4 class="h4 mb-2">
              <span class="text-gray-800"></span> Revenue Teams
            </h4>
            <p class="text-lg text-gray-800 text-center">
              Whether it's the first intro call or fifth renewal, Foresight arms
              your revenue teams with a personalized guide on how to sell each
              unique buyer.
            </p>
          </div>

          <!-- 2nd item -->
          <div
            class="relative flex flex-col items-center"
            data-aos="fade-up"
            data-aos-delay="200"
          >
            <div
              aria-hidden="true"
              class="
                absolute
                h-1
                border-t border-dashed border-gray-700
                hidden
                md:block
              "
              style="
                width: calc(100% - 32px);
                left: calc(50% + 48px);
                top: 32px;
              "
              data-aos="fade-in"
              data-aos-delay="400"
            ></div>
            <img
              class="mx-auto"
              src="../../assets/images/marketing.png"
              width="75"
              height="75"
              alt="Marketing Teams"
            />
            <h4 class="h4 mb-2">
              <span class="text-gray-800"></span> Marketing Teams
            </h4>
            <p class="text-lg text-gray-800 text-center">
              With granular data on how each user and buyer realizes value,
              Marketing teams are able to personalize based on what matters to
              each persona.
            </p>
          </div>

          <!-- 3rd item -->
          <div
            class="relative flex flex-col items-center"
            data-aos="fade-up"
            data-aos-delay="400"
          >
            <img
              class="mx-auto"
              src="../../assets/images/product.png"
              width="75"
              height="75"
              alt="Product Teams"
            />
            <h4 class="h4 mb-2">
              <span class="text-gray-800"></span> Product Teams
            </h4>
            <p class="text-lg text-gray-800 text-center">
              With a live and evolving set of user research data, product teams
              can build knowing they will drive the biggest business impact.
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Process",
};
</script>