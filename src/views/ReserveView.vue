<template>
  <main class="reserve">
    <div class="card-container">
      <div class="img-container">
        <img src="../assets/images/大阪街頭.jpg" alt="大阪街頭" />
      </div>
      <div class="text">
        <h2>大阪旅遊</h2>
        <p>日本環球影城瑪利歐～奈良東大寺.梅花鹿公園.嵐山渡月橋五日</p>
        <div class="price">
          TWD
          <span>37000</span>
          人/起
        </div>
      </div>
    </div>
    <div class="card-container">
      <div class="img-container">
        <img src="../assets/images/北海道雪景.jpg" alt="北海道雪景" />
      </div>
      <div class="text">
        <h2>北海道旅遊</h2>
        <p>洞爺湖.昭和新山.函館夜景.海洋公園.企鵝遊行.小樽運河五日</p>
        <div class="price">
          TWD
          <span>40000</span>
          人/起
        </div>
      </div>
    </div>
    <div class="card-container">
      <div class="img-container">
        <img src="../assets/images/京都古城.jpg" alt="京都古城" />
      </div>
      <div class="text">
        <h2>京都古城</h2>
        <p>暢遊龍安寺、清水寺、二條城等京都古城三日</p>
        <div class="price">
          TWD
          <span>25000</span>
          人/起
        </div>
      </div>
    </div>
    <div class="card-container">
      <div class="img-container">
        <img src="../assets/images/富士山.jpg" alt="富士山" />
      </div>
      <div class="text">
        <h2>東京旅遊</h2>
        <p>東京迪士尼.西湖合掌村.富士山纜車.東京鐵塔.溫泉購物五日</p>
        <div class="price">
          TWD
          <span>35900</span>
          人/起
        </div>
      </div>
    </div>
    <div class="card-container">
      <div class="img-container">
        <img src="../assets/images/日本壽司.jpg" alt="日本壽司" />
      </div>
      <div class="text">
        <h2>日本美食團</h2>
        <p>饕客最愛日本美食二日</p>
        <div class="price">
          TWD
          <span>15000</span>
          人/起
        </div>
      </div>
    </div>
    <div class="card-container">
      <div class="img-container">
        <img src="../assets/images/清水寺.jpg" alt="清水寺" />
      </div>
      <div class="text">
        <h2>清水寺</h2>
        <p>清水寺當日來回</p>
        <div class="price">
          TWD
          <span>10000</span>
          人/起
        </div>
      </div>
    </div>
  </main>
</template>

<script>
export default {
  name: "ReserveView",
};
</script>

<style lang="scss" scoped>
main {
  background-color: #fff;
  padding: 2rem;
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  .card-container {
    border: 1px solid lightgray;
    border-radius: 10px;
    overflow: hidden;
    width: 400px;
    height: 400px;
    margin: 1rem;
    box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.2);
    &:hover {
      box-shadow: 3px 3px 10px rgba(0, 0, 0, 0.5);
    }
    .img-container {
      height: 60%;
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
    .text {
      padding: 0.5rem;
      height: 40%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      h2 {
        font-size: 2rem;
        font-weight: 600;
      }
      .price {
        text-align: end;
        margin: 0;
        color: gray;
        span {
          font-size: 30px;
          font-weight: 600;
          color: red;
        }
      }
    }
  }
}
</style>
