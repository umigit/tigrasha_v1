<template>
  <section class="container">
    <div class="top-container">
      <div class="description">
        <img class="top-icon" src="~/assets/images/icon-white.png"/>
        <h1 class="welcome">チグラーシャへようこそ！</h1>
        <div class="QandA">
          <h2>これはなんのサイト？</h2>
          <p>　このサイトはGPSの位置情報を利用した「迷い猫捜索システム」です。</p>
          <h2>このサイトで出来ること</h2>
          <h3>1. 張り紙</h3>
          <p>　張り紙をイメージした捜索依頼を投稿することが出来ます。</p>
          <h3>2. 投稿情報の提供</h3>
          <p>　あなたの目撃した猫ちゃんの情報を投稿することが出来ます。</p>
        </div>
      </div>
      <div class="start">
        <div class="start-mask">
          <div class="top-buttons">
            <nuxt-link to="posts" class="top-button">貼り紙を見る</nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {

}
</script>

<style>
h1 {
  font-size: 34px;
  text-align: center;
  margin-top: 20px;
}

h2, h3 {
  margin-top: 10px;
  text-align: left;
}

.top-container {
  min-height: 100vh;
  height: 100%;
  color: white;
  display: flex;
  flex-wrap: wrap;
}

.top-icon {
  height: 100px;
  width: 100%;
  object-fit: contain;
}

.description {
  background-color: darkorange;
  min-height: 100vh;
  height: 100%;
  width: 50%;
  padding: 40px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.QandA {
  margin-top: 30px;
}

.start {
  background-image: url("~assets/images/tigrasha.jpg");
  background-size: cover;
  background-position: center center;
  width: 50vw;
}

.start-mask {
  background-color: rgba(0,0,0,0.5);
  min-height: 100vh;
  height: 100%;
  width: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.top-button {
  box-sizing: border-box;
  color: #fff;
  background-color: darkred;
  width: 200px;
  height: 50px;
  margin: 0 auto;
  border: 0;
  display: block;
  font-size: 20px;
  font-weight: bold;
  line-height: 50px;
  text-align: center;
  text-decoration: none;
}

@media screen and (max-width: 480px) {
  .top-container {
    flex-direction: column;
  }

  .description {
    width: 100vw;
  }

  .start {
    width: 100vw;
  }

  h1 {
    font-size: 20px;
  }

  h2 {
    font-size: 18px;
  }

  h3 {
    font-size: 16px;
  }

  p {
    font-size: 12px;
  }
}
</style>
