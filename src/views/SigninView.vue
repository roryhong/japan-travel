<template>
  <main class="login">
    <form>
      <h1>會員註冊</h1>
      <div class="email">
        <label for="email">Email:</label>
        <input type="text" id="email" />
      </div>
      <div class="password">
        <label for="password">密碼:</label>
        <input type="password" id="password" />
      </div>
      <div class="passwordAgain">
        <label for="passwordAgain">再次輸入密碼:</label>
        <input type="password" id="passwordAgain" />
      </div>
      <div class="buttonContainer">
        <button>註冊</button>
      </div>
      <div class="login">
        已是會員嗎?
        <router-link to="/login">點此登入!</router-link>
      </div>
    </form>
    <router-view></router-view>
  </main>
</template>

<script>
export default {
  name: "SigninView",
};
</script>

<style lang="scss" scoped>
$themeColor: #6e6eff;
$secondaryColor: #3b3bff;

form {
  background-color: #fff;
  padding: 2rem;
  height: 70vh;
  display: flex;
  flex-direction: column;
  h1 {
    margin: 1rem 0;
    font-size: 50px;
    font-weight: 600;
    text-align: center;
  }
  div {
    padding: 0 2rem;
    margin: 0.5rem auto;
    width: 400px;
    label {
      display: block;
      margin-bottom: 0.5rem;
      font-size: 20px;
    }
    input {
      width: 100%;
      height: 30px;
      padding: 0.5rem;
      border: 1px solid darkgray;
      border-radius: 5px;
      outline: none;
    }
  }
  .buttonContainer {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    button {
      width: 200px;
      padding: 0.5rem 0;
      margin: 1rem 0 0.5rem 0;
      font-size: 20px;
      background-color: $themeColor;
      color: #fff;
      border: none;
      border-radius: 5px;
      cursor: pointer;
      &:hover {
        background-color: $secondaryColor;
      }
    }
  }
  .login {
    margin-top: 1rem;
    a {
      text-decoration: none;
      color: $themeColor;
      &:hover {
        color: $secondaryColor;
      }
    }
  }
}
</style>
