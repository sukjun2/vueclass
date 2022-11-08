<template>
    <section id="sliderType" class="slider__wrap" :class="fonts">
        <div class="slider__inner">
            <swiper
                :spaceBetween="30"
                :centeredSlides="true"
                :autoplay="{
                    delay: 2500,
                    disableOnInteraction: false,
                }"
                :pagination="{
                    clickable: true,
                }"
                :navigation="true"
                :modules="modules"
                class="mySwiper"
            >
                <swiper-slide>
                    <div class="swiper-slide" :class="titles[0].img">
                        <div class="desc">
                            <span>{{titles[0].subtitle}}</span>
                            <h3>{{titles[0].title}}</h3>
                            <p>
                                {{titles[0].text}}
                            </p>
                            <div class="btn">
                                <a href="/">자세히 보기</a>
                                <a href="/" class="black"> 사이트 보기 </a>
                            </div>
                        </div>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="swiper-slide" :class="titles[1].img">
                        <div class="desc">
                            <span>{{titles[1].subtitle}}</span>
                            <h3>{{titles[1].title}}</h3>
                            <p>
                                {{titles[1].text}}
                            </p>
                            <div class="btn">
                                <a href="/">자세히 보기</a>
                                <a href="/" class="black"> 사이트 보기 </a>
                            </div>
                        </div>
                    </div>
                </swiper-slide>
                <swiper-slide>
                    <div class="swiper-slide" :class="titles[2].img">
                        <div class="desc">
                            <span>{{titles[2].subtitle}}</span>
                            <h3>{{titles[2].title}}</h3>
                            <p>
                                {{titles[2].text}}
                            </p>
                            <div class="btn">
                                <a href="/">자세히 보기</a>
                                <a href="/" class="black"> 사이트 보기 </a>
                            </div>
                        </div>
                    </div>
                </swiper-slide>
                <!-- <swiper-slide>
                    <div class="swiper-slide img2">
                        <div class="desc">
                            <span>BLESSING</span>
                            <h3>WEDDING SEASON</h3>
                            <p>
                                웨딩 시즌이 다가왔어요! 9월부터 시작해서 10월, 11월에도!
                                <br />
                                결혼식이 너무 많아서 지갑이 점점 가벼워지네요!
                            </p>
                            <div class="btn">
                                <a href="/">자세히 보기</a>
                                <a href="/" class="black"> 사이트 보기 </a>
                            </div>
                        </div>
                    </div>
                </swiper-slide>
                <swiper-slide
                    ><div class="swiper-slide img3">
                        <div class="desc">
                            <span>BLESSING</span>
                            <h3>WEDDING SEASON</h3>
                            <p>
                                웨딩 시즌이 다가왔어요! 9월부터 시작해서 10월, 11월에도!
                                <br />
                                결혼식이 너무 많아서 지갑이 점점 가벼워지네요!
                            </p>
                            <div class="btn">
                                <a href="/">자세히 보기</a>
                                <a href="/" class="black"> 사이트 보기 </a>
                            </div>
                        </div>
                    </div>
                </swiper-slide> -->
            </swiper>
        </div>
    </section>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from "swiper/vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/pagination";
import "swiper/css/navigation";

// import required modules
import { Autoplay, Pagination, Navigation } from "swiper";

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
            modules: [Autoplay, Pagination, Navigation],
        };
    },
    props: {
        fonts: String,
    },
    data: function () {
        return {
            titles: [
                {img: "img1", subtitle: "BLESSING", title: "WEDDING SEASON", text: "웨딩 시즌이 다가왔어요! 9월부터 시작해서 10월, 11월에도! 결혼식이 너무 많아서 지갑이 점점 가벼워지네요!"},
                {img: "img2", subtitle: "BLESSING", title: "WEDDING SEASON", text: "웨딩 시즌이 다가왔어요! 9월부터 시작해서 10월, 11월에도! 결혼식이 너무 많아서 지갑이 점점 가벼워지네요!"},
                {img: "img3", subtitle: "BLESSING", title: "WEDDING SEASON", text: "웨딩 시즌이 다가왔어요! 9월부터 시작해서 10월, 11월에도! 결혼식이 너무 많아서 지갑이 점점 가벼워지네요!"},
            ]
        }
    }
};
</script>

<style>
/* swiper */
.swiper-slide.img1 {
    background: url(../../assets/img/w_slider_bg01.jpg) no-repeat center / cover;
    margin-top: 50px;
}

.swiper-slide.img2 {
    background: url(../../assets/img/w_slider_bg02.jpg) no-repeat center / cover;
    margin-top: 50px;
}

.swiper-slide.img3 {
    background: url(../../assets/img/w_slider_bg03.jpg) no-repeat center / cover;
    margin-top: 50px;
}

.swiper-slide .desc {
    width: 1160px;
    margin: 0 auto;
    padding: 100px 20px;
    box-sizing: border-box;
}

.swiper-slide .desc span {
    font-size: 16px;
    background-color: #fac4f8;
    padding: 1px 14px 0 14px;
    border-radius: 30px;
    text-transform: uppercase;
    margin-bottom: 10px;
    display: inline-block;
}

.swiper-slide .desc h3 {
    font-size: 110px;
    font-weight: 300;
    line-height: 1;
    color: #fff;
    text-transform: uppercase;
    margin-bottom: 16px;
    margin-left: -8px;
}

.swiper-slide .desc p {
    font-size: 20px;
    font-weight: 300;
    color: #fff;
    line-height: 1.35;
    margin-bottom: 130px;
}

.swiper-slide .desc .btn a {
    font-size: 16px;
    background-color: #fff;
    padding: 11px 50px;
    display: inline-block;
    border-radius: 5px;
}

.swiper-slide .desc .btn a.black {
    background: #000;
    color: #fff;
}

.swiper-button-next,
.swiper-button-prev {
    width: 30px !important;
    height: 56px !important;
    background: url(../../assets/img/slider_icon.svg);
}

.swiper-button-next {
    background-position: -50px 0;
}

.swiper-button-next:after,
.swiper-button-prev:after {
    opacity: 0;
}

.swiper-pagination-bullet {
    width: 16px !important;
    height: 16px !important;
    background-image: url(../../assets/img/slider_icon.svg) !important;
    background-position: -20px -70px !important;
    background-color: transparent !important;
    opacity: 1 !important;
}

.swiper-pagination-bullet-active {
    background-position: 0px -70px !important;
}

.swiper-button {
    position: absolute;
    left: 50%;
    margin-left: 40px;
    bottom: 24px;
    z-index: 1000;
    display: flex;
}

.swiper-button-stop {
    background: url(../../assets/img/slider_icon.svg);
    background-position: -60px -70px;
    width: 16px;
    height: 16px;
    cursor: pointer;
}

.swiper-button-play {
    background: url(../../assets/img/slider_icon.svg);
    background-position: -40px -70px;
    width: 16px;
    height: 16px;
    cursor: pointer;
}

/* media */
@media (max-width: 960px) {
    .swiper-slide .desc {
        width: 100%;
        text-align: center;
    }

    .swiper-slide .desc h3 {
        font-size: 70px;
    }
}

@media (max-width: 600px) {
    .swiper-slide .desc {
        padding: 80px 0;
    }

    .swiper-slide .desc h3 {
        font-size: 40px;
    }

    .swiper-slide .desc p {
        font-size: 16px;
        margin-bottom: 50px;
    }

    .swiper-slide .desc .btn a {
        padding: 10px 25px;
    }
}
</style>
