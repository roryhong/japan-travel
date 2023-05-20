<template>
  <main class="contact">
    <form>
      <div class="sendEmail">
        <label for="email">寄送email給我們:</label>
        <input type="text" id="email" placeholder="輸入您的email" />
        <textarea
          cols="10"
          rows="10"
          placeholder="請留下您的寶貴意見及建議"
        ></textarea>
      </div>
      <button>送出</button>
    </form>
  </main>
</template>
<script>
export default {
  name: "ContactView",
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
  align-items: center;
  .sendEmail {
    padding: 1rem 2rem;
    margin: 0.5rem auto;
    width: 600px;
    label {
      display: block;
      margin-bottom: 1rem;
      font-size: 40px;
      font-weight: 600;
    }
    input {
      width: 100%;
      height: 30px;
      padding: 0.5rem;
      border: 1px solid darkgray;
      border-radius: 5px;
      outline: none;
    }
    textarea {
      margin-top: 1.5rem;
      width: 100%;
      padding: 0.5rem;
      border-radius: 5px;
      resize: none;
      outline: none;
      border: 1px solid #ababab;
    }
  }
  button {
    width: 200px;
    padding: 0.5rem 0;
    margin: 1rem 0;
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

@media screen and (min-width: 1000px) {
  .container {
    flex-direction: row;
    justify-content: center;
    span {
      margin: 0 5rem;
    }
  }
}
</style>
