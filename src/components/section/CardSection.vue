<template>
    <section id="cardType" class="card__wrap nexon section parallax">
        <h2>WEDDING MAKEUP</h2>
        <p>WEDDING MAKEUP의 종류, 특징, 가격 등 다양한 정보를 알아보세요.</p>
        <div class="card__inner container">
            <article class="card">
                <figure class="card__header">
                    <img src="../../assets/img/w_card_bg01_01.jpg" alt="메이크업 종류" />
                </figure>
                <div class="card__body">
                    <h3 class="tit">웨딩 메이크업 종류</h3>
                    <p class="desc">
                        일반 웨딩홀은 홍조를 살짝 띈 밝고 화사한 메이크업, 호텔은 내추럴한 피부표현으로 은은하고 고급스러운 메이크업, 채플 웨딩홀은 피부톤은 한 단계 밝게, 음영을 넣어...
                    </p>
                    <a class="btn" href="/">
                        더 자세히 보기
                        <span aria-hidden="true">
                            <svg width="65" height="8" viewBox="0 0 65 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645
                                        0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645 
                                        7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                                    fill="black"
                                />
                            </svg>
                        </span>
                    </a>
                </div>
            </article>
            <article class="card">
                <figure>
                    <img src="../../assets/img/w_card_bg01_02.jpg" alt="메이크업 특징" />
                </figure>
                <div class="card__body">
                    <h3 class="tit">웨딩 메이크업 특징</h3>
                    <p class="desc">웨딩 메이크업은 정형화된 스타일에서 점차 내추럴한 메이크업이 유행되어 차분하고 은은한 아이메이크업과 입술 색을 살린 누드 톤의 글로시한 립메이크업이 유행...</p>
                    <a class="btn" href="/">
                        더 자세히 보기
                        <span aria-hidden="true">
                            <svg width="65" height="8" viewBox="0 0 65 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645
                                        0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645
                                        7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                                    fill="black"
                                />
                            </svg>
                        </span>
                    </a>
                </div>
            </article>
            <article class="card">
                <figure>
                    <img src="../../assets/img/w_card_bg01_03.jpg" alt="메이크업 종류" />
                </figure>
                <div class="card__body">
                    <h3 class="tit">웨딩 메이크업 가격</h3>
                    <p class="desc">웨딩 헤어/메이크업은 건당 비용이 달라져요. 숨고 내에서 거래되는 웨딩 헤어/메이크업의 평균 비용은 건당 203,000원이에요. 최저 비용은 120,000원이고 최고...</p>
                    <a class="btn" href="/">
                        더 자세히 보기
                        <span aria-hidden="true">
                            <svg width="65" height="8" viewBox="0 0 65 8" fill="none" xmlns="http://www.w3.org/2000/svg">
                                <path
                                    d="M64.3536 4.35355C64.5488 4.15829 64.5488 3.84171 64.3536 3.64645L61.1716 0.464466C60.9763 0.269204 60.6597 0.269204 60.4645
                                        0.464466C60.2692 0.659728 60.2692 0.976311 60.4645 1.17157L63.2929 4L60.4645 6.82843C60.2692 7.02369 60.2692 7.34027 60.4645
                                        7.53553C60.6597 7.7308 60.9763 7.7308 61.1716 7.53553L64.3536 4.35355ZM0 4.5H64V3.5H0V4.5Z"
                                    fill="black"
                                />
                            </svg>
                        </span>
                    </a>
                </div>
            </article>
        </div>
    </section>
</template>

<style>
/* cardType */
.card__inner {
    display: flex;
    justify-content: space-between;
}

.card {
    width: 32%;
    background: #f5f5f5;
}

.card__body {
    padding: 24px;
}

.card__body .tit {
    font-size: 24px;
    margin-bottom: 10px;
    overflow: hidden;
    white-space: nowrap;
    text-overflow: ellipsis;
    padding-right: 20px;
}

.card__body .desc {
    font-size: 18px;
    line-height: 1.4;
    color: #666;
    margin-bottom: 20px;
    font-weight: 300;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 4;
    -webkit-box-orient: vertical;
}

/* media */
@media (max-width: 960px) {
    .card__inner {
        flex-wrap: wrap;
    }

    .card {
        width: 49%;
    }

    .card:last-child {
        display: none;
    }
}

@media (max-width: 600px) {
    .card {
        width: 100%;
    }

    .card:first-child {
        margin-bottom: 20px;
    }

    .card__body {
        padding: 20px;
    }

    .card__body .desc {
        font-size: 16px;
    }
}
</style>
