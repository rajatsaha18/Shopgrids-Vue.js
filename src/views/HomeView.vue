<template>
  <div class="home">




<HeroSection/>
<FeaturedSection/>
<TrendingSection/>
<BannerSection/>
<SpecialOfferSection/>
<HomeProduct/>
<BrandSection/>
<BlogSection/>
<ShippingSection/>

  </div>
</template>

<script>
import HeroSection from "@/components/home/HeroSection";
import FeaturedSection from "@/components/home/FeaturedSection";
import TrendingSection from "@/components/home/TrendingSection";
import BannerSection from "@/components/home/BannerSection";
import SpecialOfferSection from "@/components/home/SpecialOfferSection";
import HomeProduct from "@/components/home/HomeProduct";
import BrandSection from "@/components/home/BrandSection";
import BlogSection from "@/components/home/BlogSection";
import ShippingSection from "@/components/home/ShippingSection";
export default {
  name: 'HomeView',
  components: {HeroSection,FeaturedSection,TrendingSection,BannerSection,SpecialOfferSection,HomeProduct,BrandSection,BlogSection,ShippingSection}
}
</script>

<style scoped>

</style>
