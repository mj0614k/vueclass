<template>
  <section id="imageType" class="image__wrap" :class="attr">
    <h2>{{title}}</h2>
    <p>{{desc}}</p>
    <div class="image__inner" :class="layout">
      <div class="image" :class="text.img"
      v-for="text in texts" v-bind:key="text.text">
        <h3 class="image__title">{{text.title}}</h3>
        <p class="image__desc">{{text.desc}}</p>
        <a class="image__btn" :class="text.class" :href="text.link" title="자세히 보기">
          <div class="more">자세히 보기</div>
        </a>
      </div>
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
      title: "귀여운 댕댕이",
      desc: "뭐니뭐니해도 귀여운 동물 하면 강아지죠. 우선 강아지들을 보세요.",
      texts: [
        {
          img: "img1",
          title: "Shih Tzu",
          desc: "표정이 약간 멍청해 보이는 게 정말 귀엽습니다. 실제로도 멍청할 것 같습니다.",
          link: "/",
          class: ""
        },
        {
          img: "img2",
          title: "French Bulldog",
          desc: "볼수록 매력있는 견종입니다. 침을 아주 줄줄 흘린다고 합니다. 그래도 귀엽죠?",
          link: "/",
          class: "blue"
        }
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
  color: white;
  padding: 200px 30px 30px 30px;
  box-sizing: border-box;
}
.image.img1 {
  background: url(../../assets/img/img01_bg01.jpg) no-repeat center / cover;
}
.image.img2 {
  background: url(../../assets/img/img01_bg02.jpg) no-repeat center / cover;
}
.image__title {
  font-size: 32px;
  margin-bottom: 10px;
}
.image__desc {
  font-size: 18px;
  font-weight: 300;
  margin-bottom: 10px;
  line-height: 1.5;
}
.image__btn {
  font-size: 16px;
  color: #fff;
  background: #e86e47;
  padding: 10px 20px;
  display: inline-block;
}
.image__btn.blue {
  background: #00a8e5;
}
@media (max-width: 768px) {
  .image__inner {
    flex-direction: column;
  }
  .image {
    width: 100%;
  }
  .image__title {
    font-size: 24px;
    margin-bottom: 10px;
  }
  .image__desc {
    font-size: 16px;
  }
}
</style>
