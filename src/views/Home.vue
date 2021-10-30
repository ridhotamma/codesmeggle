<template>
  <main>
  <HeroSection />
  <FeatureSection />
  <FooterSection/>
  </main>
</template>

<script>
import HeroSection from "../components/HeroSection.vue"
import FeatureSection from "../components/FeatureSection.vue"
import FooterSection from "../components/FooterSection.vue"
export default {
  name: 'Home',
  components: {
    HeroSection,
    FeatureSection,
    FooterSection
  }
}
</script>

<style lang="scss" scoped>
 
</style>
