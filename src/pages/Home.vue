<template>
  <div class="flex flex-col min-h-screen overflow-hidden">
    <!-- Site header -->
    <Header />

    <!-- Page content -->
    <main class="flex-grow">
      <!-- Page illustration -->
      <div
        class="relative max-w-6xl mx-auto h-0 pointer-events-none"
        aria-hidden="true"
      >
        <PageIllustration />
      </div>

      <!-- Page sections -->
      <HeroHome />
      <Process />
      <FeaturesHome />
      <Tabs />
      <Target />
      <News />
      <Newsletter />
    </main>

    <!-- Site footer -->
    <Footer />
  </div>
</template>

<script>
import Header from "./../partials/Header.vue";
import PageIllustration from "./../partials/PageIllustration.vue";
import HeroHome from "./../partials/HeroHome.vue";
import Process from "./../partials/Process.vue";
import FeaturesHome from "./../partials/FeaturesHome.vue";
import Tabs from "./../partials/Tabs.vue";
import Footer from "./../partials/Footer.vue";

export default {
  name: "Home",
  components: {
    Header,
    PageIllustration,
    HeroHome,
    Process,
    FeaturesHome,
    Tabs,
    Footer,
  },
};
</script>
