<template>
  <div class="container">
    <div>
      <logo />
      <h1 class="title">
        podcast
      </h1>
      <h2 class="subtitle">
        Tambourine Podcast Site
      </h2>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          class="button--green"
        >Documentation</a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          class="button--grey"
        >GitHub</a>
        <!-- audio tag - export以降にmp3ファイルのid(drive)を入れてやると再生できる -->
        <audio preload="auto" controls>
          <source src="http://drive.google.com/uc?export=view&id=1qpo6qpMScDKTNcKaekUoO4_WfirF_Jaa" type="audio/mp3">
        </audio>
        <!-- driveの埋め込みコード -->
        <iframe src="https://drive.google.com/file/d/1qpo6qpMScDKTNcKaekUoO4_WfirF_Jaa/preview" width="350" height="70">
        </iframe>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
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
</style>
