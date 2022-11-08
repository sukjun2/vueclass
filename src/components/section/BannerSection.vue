<template>
    <section id="bannerType" class="banner__wrap" :class="attr">
        <h2 class="blind">배너 영역</h2>
        <div class="banner__inner">
            <h3 class="title">{{title.title}}</h3>
            <p class="desc">
                {{title.desc}}
                <a href="https://sukjun2.tistory.com/" title="티스토리로 이동">{{title.link}}</a>
            </p>
            <span class="small">{{title.small}}</span>
        </div>
    </section>
</template>

<script>
export default {
    props: {
        attr: String,
    },
    data: function () {
        return {
            title: {title: "WEDDING", desc: "There is a lot of pressure to get married during Chuseok I won't be able to remain mentally.", link: "https://sukjun2.tistory.com/", small: "추석은 압박의 명절"}
        }
    }
};
</script>

<style>
/* bannerType */
.banner__inner {
    background-image: url(../../assets/img/w_banner_bg01.jpg);
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    text-align: center;
    padding: 120px 0;
    color: #fff;
}

.banner__inner .title {
    font-size: 50px;
    line-height: 1;
    font-weight: 300;
    margin-bottom: 40px;
}

.banner__inner .desc {
    font-size: 24px;
    line-height: 1.5;
    font-weight: 300;
    margin-bottom: 70px;
}

.banner__inner .desc a {
    color: #fff;
    display: block;
}

.banner__inner .desc a:hover {
    text-decoration: underline;
}

.banner__inner .small {
    font-size: 16px;
    text-decoration: underline;
}

@media (max-width: 960px) {
    .banner__inner {
        padding: 100px 0;
    }
}

@media (max-width: 600px) {
    .banner__inner {
        padding: 80px 0;
    }

    .banner__inner .title {
        font-size: 30px;
        margin-bottom: 20px;
    }

    .banner__inner .desc {
        font-size: 16px;
        margin-bottom: 40px;
    }
}
</style>
