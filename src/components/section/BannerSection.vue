<template>
  <section id="bannerType" class="banner__wrap" :class="attr">
    <h2 class="blind">배너 영역</h2>
    <div class="banner__inner">
      <h3 class="title">잘 보셨나요?</h3>
      <p class="desc">
        이제 현실을 직시하시고, 아래의 주소를 눌러 깃허브로 이동하세요.
        <a href="https://github.com/" title="깃허브 페이지로 이동">
          github.com
        </a>
      </p>
      <span class="small">Get out and do homework!</span>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    attr: String,
  },
};
</script>
<style>
.banner__inner {
  background-image: url(../../assets/img/banner01_bg01.jpg);
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;
  padding: 120px 0;
  color: black;
}
.banner__inner .title {
  font-size: 50px;
  line-height: 1;
  font-weight: 500;
  margin-bottom: 40px;
}
.banner__inner .desc {
  font-size: 24px;
  line-height: 1.5;
  font-weight: 300;
  margin-bottom: 70px;
  word-break: keep-all;
}
.banner__inner .desc a {
  color: black;
  display: block;
}
.banner__inner .desc a:hover {
  text-decoration: underline;
}
.banner__inner .small {
  font-size: 16px;
  text-decoration: underline;
}
@media (max-width: 786px) {
  .banner__inner .title {
    font-size: 42px;
  }
  .banner__inner .desc {
    font-size: 18px;
  }
}
</style>
