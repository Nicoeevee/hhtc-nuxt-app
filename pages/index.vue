<template>
  <div class="container">
    <div class="carousel">
      <el-carousel :interval="5000" arrow="always">
        <el-carousel-item v-for="item in img" :key="item">
          <img :src="item"/>
        </el-carousel-item>
      </el-carousel>
    </div>
    <Nuxt></Nuxt>
  </div>
</template>

<script>
export default {
  layout: 'default',
  data() {
    return {
      img: [
        require("../assets/img1.png"),
        require("../assets/img4.png")
      ],
    };
  },
}
</script>

<style>

.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: 'Quicksand',
  'Source Sans Pro',
  -apple-system,
  BlinkMacSystemFont,
  'Segoe UI',
  Roboto,
  'Helvetica Neue',
  Arial,
  sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
.carousel {
  width: 1200px;
  height: 400px;
  margin: 0 auto;
  margin-top: 10px;
}

.carousel img {
  width: 100%;
  height: 100%;
}
</style>
