<template>
  <section id="footerType" class="footer__wrap" :class="attr">
    <h2 class="blind">푸터 영역</h2>
    <div class="footer__inner" :class="layout">
      <div class="footer__menu">
        <div>
          <h3>CUTE</h3>
          <ul>
            <li>
              <a href="/">MAIN</a>
            </li>
            <li>
              <a href="/">DOG</a>
            </li>
            <li>
              <a href="/">CAT</a>
            </li>
            <li>
              <a href="/">BANNER</a>
            </li>
            <li>
              <a href="/">ETC</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>DOG</h3>
          <ul>
            <li>
              <a href="/">Shih Tzu</a>
            </li>
            <li>
              <a href="/">French Bulldog</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>CAT</h3>
          <ul>
            <li>
              <a href="/">Bite</a>
            </li>
            <li>
              <a href="/">Punch</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>MORE</h3>
          <ul>
            <li>
              <a href="/">Dolphin</a>
            </li>
            <li>
              <a href="/">Raccoon</a>
            </li>
            <li>
              <a href="/">Pig</a>
            </li>
          </ul>
        </div>
        <div>
          <h3>ETC</h3>
          <ul>
            <li>
              <a href="/">Sloth</a>
            </li>
            <li>
              <a href="/">Chameleon</a>
            </li>
            <li>
              <a href="/">Meerkat</a>
            </li>
            <li>
              <a href="/">Koala</a>
            </li>
            <li>
              <a href="/">Penguin</a>
            </li>
            <li>
              <a href="/">Alpaca</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer__right">
        2022 mo0647. Portfolio is Power
        <br />
        All rights reserved.
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
.footer__wrap {
  background-color: #f5f5f5;
  width: 100%;
  padding: 50px 0;
}
.footer__menu {
  display: flex;
  margin-bottom: 30px;
  justify-content: center;
}
.footer__menu > div {
  width: 185%;
  text-align: center;
}
.footer__menu div h3 {
  font-size: 18px;
  margin-bottom: 20px;
  color: #000;
}
.footer__menu div li a {
  margin-bottom: 10px;
  display: block;
  font-size: 14px;
  color: #666;
}
.footer__right {
  border-top: 1px solid #d9d9d9;
  text-align: center;
  padding-top: 40px;
  color: #666;
  line-height: 1.5;
}
@media (max-width: 960px) {
  .footer__menu {
    display: none;
  }
  .footer__right {
    padding-top: 0;
    border-top: 0;
  }
  .footer__wrap {
    padding: 40px 0;
  }
}
</style>
