<template>
    <div>
        <HeaderLayout fonts="nexon" />
        <SliderSection fonts="nexon" />
        <ImageSection attr="section nexon" layout="container" />
        <ImgTextSection attr="nexon section gray parallax" layout="container" />
        <CardSection attr="nexon section parallax" layout="container" />
        <BannerSection attr="nexon parallax" />
        <TextSection attr="nexon section parallax" layout="container" />
        <FooterLayout attr="nexon section gray" layout="container" />
    </div>
</template>

<script>
import HeaderLayout from "./components/layout/HeaderLayout.vue";
import FooterLayout from "./components/layout/FooterLayout.vue";
import SliderSection from "./components/section/SliderSection.vue";
import ImageSection from "./components/section/ImageSection.vue";
import ImgTextSection from "./components/section/ImgTextSection.vue";
import CardSection from "./components/section/CardSection.vue";
import BannerSection from "./components/section/BannerSection.vue";
import TextSection from "./components/section/TextSection.vue";

export default {
    name: "App",
    components: {
        HeaderLayout,
        SliderSection,
        ImageSection,
        ImgTextSection,
        CardSection,
        BannerSection,
        TextSection,
        FooterLayout,
    },
};
</script>
