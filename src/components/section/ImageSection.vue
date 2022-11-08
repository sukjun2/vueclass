<template>
    <section id="imageType" class="image__wrap" :class="attr">
        <h2>{{title.subtitle}}</h2>
        <p>{{title.title}}</p>
        <div class="image__inner" :class="layout">
            <article class="image" :class="title.img" v-for="title in titles" v-bind:key="(title.img, title.title, title.desc)">
                <h3 class="image__tit">{{title.title}}</h3>
                <p class="image__desc">{{title.desc}}</p>
                <a class="image__btn" href="/" title="자세히 보기"> 자세히 보기 </a>
            </article>
            <!-- <article class="image img2">
                <h3 class="image__tit">실내 예식장</h3>
                <p class="image__desc">날씨에 구애받지 않고, 조명과 장식품의 배치에 따라 다양한 선택이 가능한 장점이 있습니다.</p>
                <a class="image__btn yellow" href="/" title="자세히 보기"> 자세히 보기 </a>
            </article> -->
        </div>
    </section>
</template>

<script>
export default {
    props: {
        attr: String,
        layout: String,
    },
    data: function () {
        return {
            title: {subtitle: "WEDDING HALL", title: "예식장은 신랑, 신부의 약속을 맺는 아름다운 장소입니다."},
            titles: [
                {img: "img1", title: "야외 예식장", desc: "일반적으로 하는 실내 예식이 아닌, 야외 예식장도 주변 경관에 따라 더욱 아름답고 분위기 있는 선택이 될 수 있습니다."},
                {img: "img2", title: "실내 예식장", desc: "날씨에 구애받지 않고, 조명과 장식품의 배치에 따라 다양한 선택이 가능한 장점이 있습니다."},
            ]
        }
    }
};
</script>

<style>
/* imageType */
.image__inner {
    display: flex;
    justify-content: space-between;
}

.image {
    width: 49%;
    height: 370px;
    color: #fff;
    padding: 200px 30px 30px 30px;
    box-sizing: border-box;
}

.image.img1 {
    background: url(../../assets/img/w_img_bg01_01.jpg) no-repeat center;
}

.image.img2 {
    background: url(../../assets/img/w_img_bg01_02.jpg) no-repeat center;
}

.image__tit {
    font-size: 32px;
    margin-bottom: 10px;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
}

.image__desc {
    font-size: 16px;
    font-weight: 300;
    margin-bottom: 10px;
    line-height: 1.5;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
}

.image__btn {
    font-size: 16px;
    color: #fff;
    background-color: #20b6a4;
    padding: 10px 20px;
    display: inline-block;
}

.image__btn.yellow {
    background-color: #386caa;
}

/* medie */
@media (max-width: 960px) {
}

@media (max-width: 600px) {
    .image__inner {
        flex-direction: column;
    }

    .image {
        width: 100%;
        padding: 210px 20px 20px 20px;
    }

    .image:first-child {
        margin-bottom: 20px;
    }

    .image__tit {
        font-size: 24px;
    }
}
</style>
