<template>
  <section id="cardType" class="card__wrap" :class="attr">
    <h2>More Cute Animal</h2>
    <p>더 다양한 동물을 원하시나요? 어떤 동물을 좋아하세요?</p>
    <div class="card__inner" :class="layout">
      <article class="card"
        v-for="text in texts"
        v-bind:key="text.text">
        <figure class="card__header">
          <img :src="text.src" :alt="text.title" />
        </figure>
        <div class="card__body">
          <h3 class="tit">{{text.title}}</h3>
          <p class="desc">
            {{text.desc}}
          </p>
          <a class="brn" :href="text.link"> 더보기 </a>
        </div>
      </article>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
    layout: String,
  },
  data() {
    return {
      title: "More Cute Animal",
      desc: "더 다양한 동물을 원하시나요? 어떤 동물을 좋아하세요?",
      texts: [
        {
          src: "../../assets/img/card_bg01.jpg",
          title: "Dolphin",
          desc: "돌고래가 그렇게 영악한 동물이라고 하죠. 근데 사실 그 커다란 바닷속에 멍청한 물고기들 사이에서 저만 똑똑한 돌고래라면 저라도 다른 물고기들을 장난감으로 생각할 것 같습니다. 지가 바다의 왕이야 뭐야... 좋은 동물인지 나쁜 동물인지 헷갈리네요.",
          link: "/"
        },
        {
          src: "../../assets/img/card_bg02.jpg",
          title: "Raccoon",
          desc: "라쿤인지 너구리인지 구별 방법은 있다지만 굳이 따지고 싶지는 않네요. 라쿤의 매력포인트는 역시 발바닥이죠. 라쿤 카페에서 악수하다가 팔찌를 빼앗겼던 안 좋은 기억이 떠오르네요. 저는 팔찌를 끼면 안 되나 봅니다.",
          link: "/"
        },
        {
          src: "../../assets/img/card_bg03.jpg",
          title: "Pig",
          desc: "아기 돼지는 참 귀엽네요. 제가 최근에 혐오스러운 돼지 머리 사진을 보고, 환장하던 순댓국을 몇 달째 끊고 있습니다. 제가 비위가 나쁜 편은 아닌데 진짜... 궁금하시면, 아래 더보기를 클릭하시면 아무것도 안 나옵니다.",
          link: "/"
        }
      ]
    }
  }
};
</script>
<style>
/* cardType */
#cardType img {
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}
.card__inner {
  display: flex;
  justify-content: space-between;
}
.card {
  width: 32%;
  background-color: #f5f5f5;
  border-radius: 10px;
}
.card__body {
  padding: 24px;
}
.card__body .tit {
  color: black;
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
.card__body a {
  text-decoration: underline;
}

@media (max-width: 1000px) {
  .card__body {
  }
}

@media (max-width: 784px) {
  .card__inner {
    flex-direction: column;
    align-items: center;
  }
  .card {
    width: 100%;
    border-radius: 0px;
  }
  #cardType img {
    border-top-left-radius: 0px;
    border-top-right-radius: 0px;
  }
  .card__body .desc {
    font-size: 16px;
  }
}
</style>
