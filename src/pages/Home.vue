<script setup>
import Header from '../partials/Header.vue'
import Hero from '../partials/Hero.vue'
import Features00 from '../partials/Features00.vue'
import Features04 from '../partials/Features04.vue'
import Features01 from '../partials/Features01.vue'
import Features02 from '../partials/Features02.vue'
import PricingTabs from '../partials/PricingTabs.vue'
import Testimonials from '../partials/Testimonials.vue'
import Cta from '../partials/Cta.vue'
import Footer from '../partials/Footer.vue'
</script>

<template>
  <div className="flex flex-col min-h-screen overflow-hidden supports-[overflow:clip]:overflow-clip">

    <!-- Site header -->
    <Header />

    <!-- Page content -->
    <main class="grow">

      <Hero />
      <Features00 />
      <Features02 />
      <Features04 />
      <Features01 />
      <Testimonials />
      <PricingTabs />

      <Cta />

    </main>
    
    <!-- Site footer -->
    <Footer />    

  </div>
</template>
