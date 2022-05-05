<template>
  <div class="footer-main">
    <center>
      <div class="footer__logo mobile-logo mt-8">
        <a href="https://coinhamster.io/">
          <img src="/logo.svg" alt="logo" />
        </a>
      </div>
    </center>
    <footer class="footer py-10">
      <div class="footer__body">
        <div class="footer__main">
          <div class="footer__logo">
            <a href="https://coinhamster.io/">
              <img src="/logo.svg" alt="logo" />
            </a>
          </div>
          <div class="footer__copyright">
            &copy; Copyright {{ new Date().getFullYear() }} HamsterCoin
          </div>
        </div>
        <div class="footer__doc--body">
          <div class="footer__doc">Documentation</div>
          <a href="/hamsterwhitepaper.pdf" download="/hamsterwhitepaper.pdf">
            White Paper
          </a>
          <a href="https://www.certik.com/projects/hamster" target="_blank">
            Certic Audit
          </a>
          <a
            href="https://bscscan.com/token/0x679d5b2d94f454c950d683d159b87aa8eae37c9e"
            target="_blank"
          >
            Bscscan
          </a>
        </div>
        <div class="footer__msgs">
          <div class="footer__doc">Follow us:</div>
          <div class="footer__msgs--body">
            <a target="_blank" href="https://twitter.com/_hamster_coin">
              <i class="fab fa-twitter"></i>
            </a>
            <a target="_blank" href="https://t.me/Hamster_Finance">
              <i class="fab fa-telegram-plane"></i>
            </a>
            <i class="fab fa-youtube"></i>
            <i class="fab fa-linkedin"></i>
            <a target="_blank" href="https://www.instagram.com/hamster_coin/">
              <i class="fab fa-instagram"></i>
            </a>
            <a target="_blank" href="https://support-79390.medium.com/">
              <i class="fab fa-medium"></i>
            </a>
            <a target="_blank" href="https://github.com/Hamstersfinance">
              <i class="fab fa-github"></i>
            </a>
          </div>
        </div>
      </div>
    </footer>
    <div class="footer__copyright text-center mobile-footer mb-8">
      &copy; Copyright {{ new Date().getFullYear() }} HamsterCoin
    </div>
  </div>
</template>

<script>
export default {
  mounted() {},
};
</script>

<style lang="scss" scoped>
.footer {
  margin-top: 30px;
  @media (max-width: 760px) {
    border-top: 0;
  }
  padding: 30px 0;
  border-top: 1px solid #7777;
  display: flex;
  justify-content: center;
  padding: 10px 20px;
  &__main {
    @media (max-width: 760px) {
      display: none;
    }
  }
  &__logo {
    width: 54px;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
    }
  }
  &__body {
    @media (max-width: 530px) {
      justify-content: center;
    }
    width: min(100%, 1920px);
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    gap: 10px;
  }

  &__copyright {
    color: #8c8c8c;
    font-size: 16px;
    margin-top: 80px;
    @media (max-width: 760px) {
      display: none;
    }
  }
  &__doc--body {
    @media (max-width: 530px) {
      text-align: center;
    }
    display: flex;
    flex-direction: column;
    a {
      font-size: 18px;
      font-weight: 400;
      text-decoration: none;
      color: #fff;
      margin-bottom: 10px;
      &:hover {
        color: #ffe59e;
      }
    }
  }
  &__doc {
    @media (max-width: 530px) {
      text-align: center;
    }
    font-size: 20px;
    font-weight: 500;
    margin-bottom: 18px;
  }
  &__msgs--body {
    display: flex;
    flex-wrap: wrap;
    gap: 10px;
    a {
      text-decoration: none;
    }
  }
  &__msgs {
    font-size: 24px;
    i {
      cursor: pointer;
      border: 1px solid #f5e6bd;
      border-radius: 50%;
      width: 40px;
      height: 40px;
      display: flex;
      justify-content: center;
      align-items: center;
      color: #f5e6bd;
      transition: color ease-in-out 0.2s;
      &:hover {
        color: #f09d3e;
      }
    }
  }
}
@media (max-width: 760px) {
  .footer-main {
    border: 1px solid #7777;
  }
}
.mobile-footer {
  display: none;
  @media (max-width: 760px) {
    display: block;
    margin-top: 0px;
    text-align: center;
  }
}
.mobile-logo {
  display: none;
  @media (max-width: 760px) {
    display: block;
  }
}
</style>
