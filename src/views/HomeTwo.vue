<template>
  <div class="main-container">
    <Header />

    <HeroOne :sliderData="data.heroTwo" />

    <AboutSection />

    <ProjectGridSlider />

    <ServiceTabs />

    <Testimonial />

    <BrandCarousel addClass="grey-bg" />

    <Footer />

    <OffCanvasMobileMenu />

    <!-- back to top start -->
    <back-to-top class="scroll-top" bottom="60px">
      <i class="ion-android-arrow-up"></i>
    </back-to-top>
    <!-- back to top end -->
  </div>
</template>

<script>
import Header from "@/components/Header";
import HeroOne from "@/components/sections/HeroOne";
import AboutSection from "@/components/sections/AboutSection";
import ProjectGridSlider from "@/components/sections/ProjectGridSlider";
import ServiceTabs from "@/components/sections/ServiceTabs";
import Testimonial from "@/components/Testimonial";
import BrandCarousel from "@/components/BrandCarousel";
import Footer from "@/components/Footer";
import OffCanvasMobileMenu from "@/components/OffCanvasMobileMenu";

import data from "../data/slider.json";
export default {
  data() {
    return {
      data
    };
  },
  components: {
    Header,
    HeroOne,
    AboutSection,
    ProjectGridSlider,
    ServiceTabs,
    Testimonial,
    BrandCarousel,
    Footer,
    OffCanvasMobileMenu
  },
  metaInfo: {
    title: "Certified Design Ltd",
    htmlAttrs: {
      lang: "en",
      amp: true
    }
  }
};
</script>
