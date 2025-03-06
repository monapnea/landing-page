<template>
  <div class="video-container">
    <video autoplay loop muted playsinline>
<!--      <source :src="videoSrc" type="video/mp4">-->
      <source :src="'/IMG_7051.mov'" type="video/mp4">
      Your browser does not support the video tag.
    </video>
    <div class="overlay"></div>
    <div class="content">
      <h1 class="title">MONAPNEA</h1>
      <p class="subtitle">Master Your Breath. Conquer the Depths.</p>
    </div>
  </div>
</template>

<!--<script>-->
// <!--import videoFile from '@/assets/IMG_7051.mov'; // Adjust path as needed-->

<!--export default {-->
<!--  data() {-->
<!--    return {-->
<!--      videoSrc: videoFile-->
<!--    };-->
<!--  }-->
<!--};-->
<!--</script>-->

<style lang="scss" scoped>
.video-container {
  position: relative;
  width: 100vw;
  height: 100vh;
  overflow: hidden;

  video {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    min-width: 100%;
    min-height: 100%;
    width: auto;
    height: auto;
    z-index: -1;
  }

  .overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: rgba(0, 0, 0, 0.5); // Dark overlay for readability
  }

  .content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    color: white;
    z-index: 2;
  }

  .title {
    color: white;
    font-size: 4rem;
    font-weight: bold;
    text-transform: uppercase;
    margin: 0;
  }

  .subtitle {
    font-size: 1.5rem;
    margin-top: 10px;
    opacity: 0.8; // Slightly transparent
  }
}
</style>