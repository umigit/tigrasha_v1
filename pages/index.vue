<template>
  <section class="container">
    <div>
      <TheHeader/>
      <div class="poster-content">
        <div class="poster-box">
          <div class="poster" v-for="post in posts" :key="post.id">
            <h2>{{post.title}}</h2>
            <img class="post-image" :src="post.image"/>
            <div class="post-text">
              <p>お名前：{{post.name}}</p>
              <p>最後に見た場所：{{post.place}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from 'axios'
import TheHeader from '~/components/TheHeader.vue'

export default {
  components: {
    TheHeader,
  },
  async asyncData({}) {
    let result = await axios.get('http://118.27.15.65/api/posts/?format=json');
    const posts = result.data;
    return { posts };
  },
}
</script>

<style>
h2 {
  text-align: center;
  margin-bottom: 10px;
}

.container {
  min-height: 100vh;
  background-image: url("~assets/images/gray-wall.jpg");
  background-size: cover;
  background-position: center center;
}

.poster-content {
  padding-top: 60px;
}

.poster-box {
  width: 1020px;
  margin: 0 auto;
  padding: 40px 0;
  display: flex;
  justify-content: center;
}

.poster {
  background-color: white;
  width: 300px;
  padding: 10px;
}

.post-image {
  width: 280px;
  height: 210px;
  object-fit: contain;
}

@media screen and (max-width: 1024px) {
  .poster-box {
    width: 800px;
  }
}

@media screen and (max-width: 896px) {
  .poster-box {
    width: 100%;
  }
}

@media screen and (max-width: 480px) {
  .poster-box {
    width: 100%;
  }
}
</style>

