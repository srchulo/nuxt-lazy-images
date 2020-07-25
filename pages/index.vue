<template>
  <div class="container">
    <div>
      <lazy-wrapper
        tag="h1"
        class="title"
        :src="require('~/assets/images/ocean.jpg')"
      >
        nuxt-lazy-images
      </lazy-wrapper>
      <h2 class="subtitle">
        My laudable Nuxt.js project
      </h2>
      <div class="links">
        <a href="https://nuxtjs.org/" target="_blank" class="button--green">
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
      <div v-for="catPic in catPics" :key="catPic" class="catPic">
        <lazy-image
          :src="require(`~/assets/images/${catPic}`)"
          width="350"
          height="350"
        />
      </div>

      <lazy-wrapper
        tag="h1"
        class="title"
        :src="require('~/assets/images/volcano.jpg')"
      >
        nuxt-lazy-images
      </lazy-wrapper>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      catPics: [
        'orange_cat.jpg',
        'sleepy_cat.jpg',
        'looking_cat.jpg',
        'feather_cat.jpg',
        'grass_cat.jpg'
      ]
    }
  }
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
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #def;
  letter-spacing: 1px;

  /* You must set a specified height */
  background-position: center center;
  /* Center the image */
  background-repeat: no-repeat;
  /* Do not repeat the image */
  background-size: cover;
  /* Resize the background image to cover the entire container */
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #fff;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.catPic {
  margin: 20px;
}
</style>
