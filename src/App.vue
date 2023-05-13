<template>
  <div id="app">
    <header>
      <section class="logo">
        <img src="./assets/Icons/網站Logo.svg" />
        <h1>2023日本旅遊推薦</h1>
      </section>
      <nav>
        <ul>
          <li>
            <router-link to="/">
              <i class="fa-solid fa-plane"></i> 日本旅遊
            </router-link>
          </li>
          <li>
            <router-link to="/login">
              <i class="fa-solid fa-right-to-bracket"></i>
              會員登入
            </router-link>
          </li>
          <li>
            <router-link to="/reserve">
              <i class="fa-solid fa-book"></i> 預約行程
            </router-link>
          </li>
          <li>
            <router-link to="/contact">
              <i class="fa-regular fa-address-book"></i> 聯絡我們
            </router-link>
          </li>
        </ul>
      </nav>
    </header>
    <router-view />
    <FooterView></FooterView>
  </div>
</template>

<script>
import FooterView from "./views/FooterView.vue";
export default {
  components: { FooterView },
};
</script>

<style lang="scss">
$themeColor: #6e6eff;

::-webkit-scrollbar {
  width: 10px;
}
::-webkit-scrollbar-track {
  background: #f1f1f1;
}
::-webkit-scrollbar-thumb {
  background-color: $themeColor;
}
::-webkit-scrollbar-thumb:hover {
  background: rgb(118, 95, 219);
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Roboto", "Noto Sans TC", sans-serif;
}
h1,
h2,
h3,
h4,
h5,
h6 {
  font-weight: normal;
}
header {
  background-color: #fff;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  position: sticky;
  top: 0;
  z-index: 10;
  box-shadow: 0 10px 6px -6px #8a8a8a;
  section.logo {
    flex: 3 1 400px;
    display: flex;
    align-items: center;
    h1 {
      font-size: 2.5rem;
    }
    img {
      width: 6vw;
      height: 6vw;
    }
  }
  nav {
    flex: 5 1 500px;
    ul {
      display: flex;
      list-style-type: none;
      justify-content: space-around;
      li {
        a {
          color: black;
          text-decoration: none;
          font-size: 1.35rem;
          transition: all 0.2s ease;
          padding-bottom: 0.2rem;
          &:hover {
            color: $themeColor;
            border-bottom: 3px solid $themeColor;
          }
        }
      }
    }
  }
}
@media screen and (max-width: 920px) {
  header {
    section.logo {
      justify-content: center;
    }
    nav {
      ul {
        li {
          padding: 0.5rem 0.25rem;
        }
      }
    }
  }
}
</style>
