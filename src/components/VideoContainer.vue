<template>
    <div class="videoContainer">
        <video class="fullscreenVideo" id="bgVid" playsinline autoplay muted loop>
            <source src="@/assets/background-video.mp4" type="video/mp4">
        </video>
        <div class="content">
            <slot></slot>
        </div>
    </div>
</template>

<script>
export default {
    name: "VideoContainer",

}
</script>

<style scoped>
.videoContainer {
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    overflow: hidden;
    cursor: url('/public/cursors/work.png') 16 16, auto;
}

#bgVid {
    width: 1%;
    height: 1%;
    position: fixed;
}

.fullscreenVideo {
    position: absolute;
    top: 0;
    left: 0;
    min-width: 100%;
    min-height: 100%;
    width: auto;
    height: auto;
    object-fit: cover;
    z-index: -1;
}

.content {
    position: relative;
    z-index: 1;
    /* 根据需要调整内容的样式，例如添加内边距 */
    padding: 20px;
}
</style>
