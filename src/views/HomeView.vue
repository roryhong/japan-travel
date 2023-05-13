<template>
  <main class="home">
    <section class="background-img" ref="img">
      <div class="filter"></div>
      <h3>
        休閒空間，特殊假期。<br />
        安排一趟日本旅遊行程，放鬆身心。
      </h3>
    </section>
    <section class="info-circles">
      <h3>遊玩主題</h3>
      <div class="circles">
        <div class="circle" v-for="(theme, index) in themes" :key="index">
          <img
            :title="theme.title"
            :src="require(`../assets/images/${theme.title}.jpg`)"
            :alt="theme.title"
          />
          <p>{{ theme.describe }}</p>
        </div>
      </div>
    </section>
    <section class="empty-container">
      <h3>今天就開始規劃行程，找到最適合的方案。</h3>
    </section>
    <section class="google-map">
      <h3>日本地理位置</h3>
      <p>
        日本在地理上屬於東北亞，東鄰太平洋，西以日本海、朝鮮海峽、東海與歐亞大陸的西伯利亞、朝鮮半島、中國大陸鄰接，南以菲律賓海與台灣、馬里亞納群島鄰接，北以宗谷海峽、鄂霍次克海與庫頁島、千島群島鄰接。日本一年四季都是舒爽怡人的氣候，四季變化分明。
        南部暖和，越往北部越寒冷。 特別是冬天吹西北季風，在日本海側會下很多雪。
        另一方面、在太平洋側會持續是被稱為「冬晴」的乾燥晴天。
      </p>
      <iframe
        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d6553741.945514398!2d131.0454658986125!3d36.67283455205923!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x34674e0fd77f192f%3A0xf54275d47c665244!2z5pel5pys!5e0!3m2!1szh-TW!2stw!4v1681305389840!5m2!1szh-TW!2stw"
        width="600"
        height="450"
        style="border: 0"
        allowfullscreen=""
        loading="lazy"
        referrerpolicy="no-referrer-when-downgrade"
      ></iframe>
    </section>
  </main>
</template>

<script>
export default {
  name: "HomeView",
  data() {
    return {
      idx: 0,
      imgsTitle: [
        "大阪街頭",
        "日本壽司",
        "日本櫻花",
        "北海道雪景",
        "京都古城",
        "清水寺",
        "富士山",
        "富士山2",
      ],
      themes: [
        { title: "日本壽司", describe: "日本道地壽司與美食" },
        { title: "北海道雪景", describe: "北海道雪景，美不勝收" },
        { title: "清水寺", describe: "京都清水寺，千年古都" },
        { title: "富士山", describe: "富士山風景與溫泉" },
      ],
    };
  },
  mounted() {
    this.$refs.img.style.backgroundImage = `url('${require(`../assets/images/${
      this.imgsTitle[this.idx]
    }.jpg`)}')`;

    const timer = setInterval(() => this.changeImg(), 3000);
    this.$once("hook:beforeDestroy", () => clearInterval(timer));
  },
  methods: {
    changeImg() {
      this.idx = this.idx + 1;
      if (this.idx >= this.imgsTitle.length - 1) {
        this.idx = 0;
      }

      this.$refs.img.style.backgroundImage = `url('${require(`../assets/images/${
        this.imgsTitle[this.idx]
      }.jpg`)}')`;
    },
  },
};
</script>
<style lang="scss" scoped>
$themeColor: #6e6eff;

main.home {
  position: relative;
  .background-img {
    min-height: 70vh;
    background-position: center;
    background-size: cover;
    transition: all 0.75s ease;
    position: relative;
    z-index: 0;
    display: flex;
    align-items: center;
    justify-content: center;
    .filter {
      background-color: rgba(0, 0, 0, 0.5);
      width: 100%;
      min-height: 70vh;
      position: absolute;
      top: 0;
      left: 0;
      z-index: -1;
    }
    h3 {
      color: white;
      font-size: 2.5rem;
      text-align: center;
    }
  }
  .info-circles {
    background-color: #fff;
    padding: 2rem 1rem;
    h3 {
      text-align: center;
      font-size: 2rem;
    }
    .circles {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      .circle {
        padding: 1rem;
        flex: 0 1 250px;
        display: flex;
        flex-direction: column;
        align-items: center;
        img {
          width: 80%;
          border-radius: 50%;
          transition: all 0.1s ease-in;
          padding: 0.3rem;
          &:hover {
            border: 3px solid $themeColor;
          }
        }
      }
    }
  }
  .empty-container {
    min-height: 70vh;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
    h3 {
      font-size: 2rem;
      color: #fff;
    }
  }
  .google-map {
    background-color: #fff;
    padding: 2rem 1rem;
    text-align: center;
    h3 {
      font-size: 2.5rem;
    }
    p {
      font-size: 1.25rem;
      margin: 1rem;
    }
    iframe {
      width: 100%;
      height: 40vh;
    }
  }
}
</style>
