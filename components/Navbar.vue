<template>
  <nav class="navbar">
    <div class="navbar__body">
      <ul class="navbar__list">
        <li class="navbar__logo">
          <a href="https://coinhamster.io">
            <img src="/logo.svg" alt="logo" />
          </a>
        </li>
        <li class="navbar__lang usa" @click="changeLangUsa">
          <img src="/usa.svg" alt="usa lang" />
        </li>
        <li class="navbar__lang turk" @click="changeLangTurk">
          <img src="/turk.svg" alt="turk lang" />
        </li>
      </ul>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    changeLangUsa() {
      this.$store.state.usa = true;
      this.$store.state.turk = false;
      document.cookie = "usa";
      location.reload();
    },
    changeLangTurk() {
      this.$store.state.turk = true;
      this.$store.state.usa = false;
      document.cookie = "turk";
      location.reload();
    },
  },
};
</script>

<style lang="scss" scoped>
.navbar {
  background-color: #f5e6bd;
  box-shadow: 0px 16px 40px rgb(185 135 0 / 50%);
  display: flex;
  justify-content: center;

  &__body {
    width: min(100%, 1920px);
    padding: 10px 20px;
  }

  &__list {
    display: flex;
    align-items: center;
    list-style-type: none;
    justify-content: center;
  }

  &__logo {
    width: 52px;
    cursor: pointer;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
    }
  }

  &__lang {
    cursor: pointer;
    width: 30px;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      object-position: center;
      transition: transform ease-in-out 0.2s;
      &:hover {
        transform: scale(1.2);
      }
    }
  }
}
.usa {
  margin-left: auto;
}
.turk {
  margin-left: 20px;
}
</style>
