<template>
    <section id="imgTextType" class="imgText__wrap" :class="attr">
        <h2 class="blind">유용한 사이트 살펴보기</h2>
        <div class="imgText__inner" :class="layout">
            <div class="imgText__txt">
                <span>{{title.subtitle}}</span>
                <h3>{{title.title}}</h3>
                <p>{{title.desc}}</p>
                <ul>
                    <li v-for="title in titles" v-bind:key="(title.link, title.text)">
                        <a :href=title.link>{{title.text}}</a>
                    </li>
                    <!-- <li>
                        <a href="/">턱시도 사이트</a>
                    </li>
                    <li>
                        <a href="/">한복 사이트</a>
                    </li>
                    <li>
                        <a href="/">드레스 사이트2</a>
                    </li>
                    <li>
                        <a href="/">턱시도 사이트2</a>
                    </li>
                    <li>
                        <a href="/">한복 사이트2</a>
                    </li> -->
                </ul>
            </div>
            <div class="imgText__img" :class="title.img" v-for="title in subtitle" v-bind:key="(title.img, title.site, title.link)">
                <a :href="title.link">{{title.site}}</a>
            </div>
            <!-- <div class="imgText__img img2">
                <a href="/" class="blue">{{subtitle.site2}}</a>
            </div> -->
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
            title: {subtitle: "WEDDING DRESS SITE", title: "WEDDING DRESS", desc: "신랑, 신부님의 턱시도 / 드레스 or 한복을 볼 수 있는 사이트입니다."},
            titles: [
                {link: "/", text: "드레스 사이트"},
                {link: "/", text: "턱시도 사이트"},
                {link: "/", text: "한복 사이트"},
                {link: "/", text: "드레스 사이트"},
                {link: "/", text: "턱시도 사이트"},
                {link: "/", text: "한복 사이트"},
            ],
            subtitle: [
                {img: "img1", site: "드레스 사이트", link: "/"},
                {img: "img2", site: "턱시도 사이트", link: "/"}
            ]
        }
    }
};
</script>

<style>
/* imgTextType */
.imgText__inner {
    display: flex;
    justify-content: space-between;
}
.imgText__inner > div {
    width: 32%;
    height: 500px;
}
.imgText__txt span {
    font-size: 16px;
    color: #666;
    text-decoration: underline;
    text-underline-position: under;
    margin-bottom: 20px;
    display: block;
}
.imgText__txt h3 {
    font-size: 50px;
    font-weight: 300;
    margin-bottom: 20px;
}
.imgText__txt p {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.5;
    color: #666;
    margin-bottom: 10px;
}
.imgText__txt ul {
    font-size: 18px;
    font-weight: 300;
    line-height: 1.6;
}
.imgText__txt ul li {
    position: relative;
    padding-left: 20px;
}
.imgText__txt ul li a {
    color: #666;
}
.imgText__txt ul li::before {
    content: "";
    width: 5px;
    height: 5px;
    border-radius: 50%;
    position: absolute;
    left: 5px;
    top: 9px;
    background: #666;
}
.imgText__img {
    border-radius: 10px;
    position: relative;
}
.imgText__img a {
    position: absolute;
    left: 30px;
    bottom: 30px;
    background-color: #ea88e6;
    color: #fff;
    font-size: 18px;
    padding: 10px 30px;
    border-radius: 30px;
    display: inline-block;
}
.imgText__img a.blue {
    background-color: #2b387c;
}
.imgText__img.img1 {
    background: url(../../assets/img/w_imgText_bg01.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
    background: url(../../assets/img/w_imgText_bg02.jpg) no-repeat center / cover;
}
/* media */
@media (max-width: 960px) {
    .imgText__inner {
        flex-wrap: wrap;
    }
    .imgText__txt h3 {
        font-size: 40px;
    }
    .imgText__txt p {
        margin-bottom: 60px;
    }
    .imgText__inner > div.imgText__txt {
        width: 100%;
        height: auto;
        text-align: center;
    }
    .imgText__inner > div.imgText__txt ul {
        display: none;
    }
    .imgText__inner > div.imgText__img {
        width: 49%;
    }
}
@media (max-width: 600px) {
    .imgText__txt span {
        font-size: 14px;
        margin-bottom: 10px;
    }
    .imgText__txt h3 {
        font-size: 30px;
    }
    .imgText__txt p {
        font-size: 16px;
        margin-bottom: 50px;
    }
    .imgText__inner > div.imgText__img {
        width: 100%;
        height: 200px;
    }
    .imgText__inner > div.imgText__img.img1 {
        margin-bottom: 20px;
    }
    .imgText__img a {
        left: 20px;
        bottom: 20px;
    }
}
</style>
