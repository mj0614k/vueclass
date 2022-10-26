<template>
  <section id="textType" class="text__wrap" :class="attr">
    <span>글로는 표현하기 힘든 귀여움</span>
    <h2>네 발 달린 동물들은 다 귀엽다</h2>
    <div class="text__inner" :class="layout">
      <div class="text t1">
        <h3 class="text__title">Sloth</h3>
        <p class="text__desc">
          남아메리카, 중앙 아메리카의 열대림에 서식하는 동물입니다. 생애의
          대부분을 나무에 매달려 보낸다고 합니다. 주*피아가 생각납니다. 못생긴
          녀석...
        </p>
        <a class="text__btn" href="/"> 더보기 </a>
      </div>
      <div class="text t2">
        <h3 class="text__title">Chameleon</h3>
        <p class="text__desc">
          변화하는 몸의 색이 특징인 동물입니다. 세계 개체 수의 절반이
          마다가스카르 섬에 산다고 합니다. 세계 개체 수는 어떻게 측정했을까요?
          괜히 이런 게 궁금합니다.
        </p>
        <a class="text__btn" href="/"> 더보기 </a>
      </div>
      <div class="text t3">
        <h3 class="text__title">Meerkat</h3>
        <p class="text__desc">
          남아프리카 공화국과 앙골라 사막에 서식합니다. 두 손을 모으고 태양열을
          흡수한다고 합니다. 미어캣 울음소리 들어보셨나요? 약간 충격적입니다.
        </p>
        <a class="text__btn" href="/"> 더보기 </a>
      </div>
      <div class="text t4">
        <h3 class="text__title">Koala</h3>
        <p class="text__desc">
          호주에 서식하는 유대류입니다. 무리를 만들지 않고 혼자 생활한다고
          합니다. 그냥 친구가 없는 건 아닐까요? 이건 어쩌면... 제 이야기일지도
          모릅니다.
        </p>
        <a class="text__btn" href="/"> 더보기 </a>
      </div>
      <div class="text t5">
        <h3 class="text__title">Penguin</h3>
        <p class="text__desc">
          펭귄은 펭귄목 펭귄과에 속하는 날지 못하는 새의 총칭입니다. 무리에서
          생활하는 사회성있는 동물로 유명합니다. 코알라와는 아주 정반대네요.
          인싸 동물.
        </p>
        <a class="text__btn" href="/"> 더보기 </a>
      </div>
      <div class="text t6">
        <h3 class="text__title">Alpaca</h3>
        <p class="text__desc">
          알파카는 본래 집단 생활을 하는 동물이라 키울 때는 반드시 두마리 짝을
          만들어서 키워야 한다고 합니다. 얘가 그 침 뱉는 애 맞죠? 더럽게 침을...
        </p>
        <a class="text__btn" href="/"> 더보기 </a>
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
};
</script>
<style>
/* textType */
.text__inner {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}
.text {
  width: 32%;
  margin-bottom: 2%;
  padding: 20px;
  box-sizing: border-box;
  border-radius: 10px;
  transition: background 0.4s;
}
.text:hover {
  background: #f5f5f5;
}
.text:hover .text__title {
  color: #000;
}
.text__title {
  font-size: 24px;
  line-height: 1;
  margin-bottom: 10px;
  text-overflow: ellipsis;
  white-space: nowrap;
  position: relative;
  padding-top: 75px;
}
.text__title::before {
  content: "";
  position: absolute;
  left: 0;
  top: 0;
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: url(../../assets/img/text01_icon01.svg);
}
.text.t1 .text__title::before {
  background-position: 0 0;
}
.text.t2 .text__title::before {
  background-position: -60px 0;
}
.text.t3 .text__title::before {
  background-position: -120px 0;
}
.text.t4 .text__title::before {
  background-position: -180px 0;
}
.text.t5 .text__title::before {
  background-position: -240px 0;
}
.text.t6 .text__title::before {
  background-position: -300px 0;
}
.text__desc {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.4;
  overflow: hidden;
  text-overflow: ellipsis;
  display: -webkit-box;
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  color: #666;
  margin-bottom: 20px;
}
.text__btn {
  font-size: 16px;
  line-height: 1;
  text-decoration: underline;
  color: #666;
}

@media (max-width: 768px) {
  #textType > span {
    display: none;
  }
  .text__desc {
    font-size: 16px;
    overflow: hidden;
    text-overflow: ellipsis;
    display: -webkit-box;
    -webkit-line-clamp: 4;
    -webkit-box-orient: vertical;
  }
  .text {
    width: 50%;
    margin-bottom: 0px;
    padding: 10px;
  }
}
</style>
