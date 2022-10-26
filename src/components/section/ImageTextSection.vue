<template>
  <section id="imgTextType" class="image__wrap" :class="attr">
    <h2 class="blind">고양이가 빠지면 섭하다</h2>
    <div class="imgText__inner" :class="layout">
      <div class="imgText__txt">
        <span>고양이 영역</span>
        <h3>고양이가 빠지면 섭하다</h3>
        <p>
          고양이가 성격은 나쁘다지만, <br />
          강아지들도 다 좋은 녀석들만은 아니잖아요.
        </p>
        <ul>
          <li>
            <a href="/">Persian</a>
          </li>
          <li>
            <a href="/">Siamese</a>
          </li>
          <li>
            <a href="/">Sphynx</a>
          </li>
          <li>
            <a href="/">ragdoll</a>
          </li>
          <li>
            <a href="/">Scottish Fold</a>
          </li>
          <li>
            <a href="/">Turkish angora</a>
          </li>
        </ul>
      </div>
      <div class="imgText__img img1">
        <a href="/">옷자락 물어뜯기기</a>
      </div>
      <div class="imgText__img img2">
        <a class="blue" href="/"> 냥냥펀치 후드려 맞기 </a>
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
  font-weight: 500;
  word-break: keep-all;
  line-height: 1.4;
  margin-bottom: 20px;
}
.imgText__txt p {
  font-size: 18px;
  font-weight: 300;
  line-height: 1.5;
  color: #666;
  margin-bottom: 10px;
  word-break: keep-all;
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
  background-color: #666;
}
.imgText__img {
  border-radius: 10px;
  position: relative;
}
.imgText__img a {
  background-color: #7c2b39;
  color: #fff;
  font-size: 20px;
  position: absolute;
  bottom: 0;
  text-align: center;
  width: 100%;
  padding: 20px 30px;
  box-sizing: border-box;
  display: inline-block;
}
.imgText__img a.blue {
  background-color: #2b387c;
}
.imgText__img.img1 {
  background: url(../../assets/img/imgText01_bg01.jpg) no-repeat center / cover;
}
.imgText__img.img2 {
  background: url(../../assets/img/imgText01_bg02.jpg) no-repeat center / cover;
}

@media (max-width: 768px) {
  .imgText__txt h3 {
    font-size: 42px;
  }
  .imgText__txt span {
    display: none;
  }
  .imgText__inner {
    display: block;
  }
  .imgText__inner > div:first-child {
    width: 100%;
    height: 400px;
    text-align: center;
  }
  .imgText__inner > div:nth-child(2),
  .imgText__inner > div:nth-child(3) {
    width: 50%;
    height: 500px;
    float: left;
    margin-bottom: 150px;

    border-radius: 0px;
  }
  .imgText__txt ul li::before {
    display: none;
  }
  .imgText__img a {
    font-size: 14px;
  }
}
</style>
