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
        <div class="start-mask"></div>
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
  font-size: 40px;
  text-align: center;
}

h2, h3 {
  margin-top: 10px;
}

.top-container {
  min-height: 100vh;
  color: white;
  background-position: center center;
  background-repeat: no-repeat;
  background-size: 200px;
  display: flex;
  align-items: center;
}

.top-icon {
  height: 100px;
  width: 100%;
  object-fit: contain;
}

.description {
  background-color: darkorange;
  height: 100vh;
  width: 50%;
  padding: 40px;
}

.QandA {
  margin-top: 30px;
}

.start {
  background-image: url("~assets/images/tigrasha.jpg");
  background-position: center center;
  background-size: 100vh;
  height: 100vh;
  width: 50vw;
}

.start-mask {
  background-color: rgba(0,0,0,0.5);
  height: 100%;
  width: 100%;
}
</style>
