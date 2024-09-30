<template>
  <VideoContainer>
    <NavBar />
    <router-view />

  </VideoContainer>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap/dist/js/bootstrap'
import NavBar from '@/components/NavBar.vue'
import VideoContainer from '@/components/VideoContainer.vue'

export default {
  name: "App",
  components: {
    NavBar,
    VideoContainer
  },

}
</script>

<style></style>
