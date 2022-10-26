<template>
    <div>
        <HeaderLayout />
        <!-- <SliderSection /> -->
        <ImageSection />
        <ImgTextSection />
        <CardSection />
        <BannerSection />
        <TextSection />
        <FooterLayout />
    </div>
</template>

<script>
import HeaderLayout from "./components/layout/HeaderLayout.vue";
import FooterLayout from "./components/layout/FooterLayout.vue";

// import SliderSection from "./components/layout/SliderSection.vue";
import ImageSection from "./components/section/ImageSection.vue";
import ImgTextSection from "./components/section/ImgTextSection.vue";
import CardSection from "./components/section/CardSection.vue";
import BannerSection from "./components/section/BannerSection.vue";
import TextSection from "./components/section/TextSection.vue";

export default {
    name: "App",
    components: {
        HeaderLayout,
        // SliderSection,
        ImageSection,
        ImgTextSection,
        CardSection,
        BannerSection,
        TextSection,
        FooterLayout,
    },
};
</script>
