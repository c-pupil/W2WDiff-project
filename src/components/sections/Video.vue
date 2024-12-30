<!--<script>-->

<!--</script>-->

<!--<template>-->
<!--  <div>-->
<!--    <el-divider />-->

<!--    <el-row justify="center">-->
<!--      <h1 class="section-title">Explainer Video</h1>-->
<!--    </el-row>-->

<!--    &lt;!&ndash; 每个网站的视频的iframe可能不一致，最好在这里手动调整 &ndash;&gt;-->
<!--    <el-row justify="center">-->
<!--      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="10" >-->
<!--        <el-container id="video-container">-->
<!--          <iframe src="//player.bilibili.com/player.html?isOutside=true&aid=802517980&bvid=BV1qy4y1x7VV&cid=325180260&p=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"></iframe>-->
<!--        </el-container>-->
<!--      </el-col>-->
<!--    </el-row>-->

<!--  </div>-->
<!--</template>-->

<!--<style scoped>-->

<!--#video-container{-->
<!--  margin: 15px 0px 0px 0px;-->
<!--}-->

<!--iframe {-->
<!--  aspect-ratio: 16 / 9;-->
<!--  height: 100%;-->
<!--  width: 100%;-->
<!--}-->

<!--</style>-->


<!--<template>-->
<!--  <div>-->
<!--    <el-divider />-->

<!--    <el-row justify="center">-->
<!--      <h1 class="section-title">Explainer Video</h1>-->
<!--    </el-row>-->

<!--    <el-row justify="center">-->
<!--      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="10">-->
<!--        <el-container id="video-container">-->
<!--          <div class="video-wrapper">-->
<!--            <video ref="video1" controls @loadedmetadata="setVideoDimensions">-->
<!--              <source src="./video/UCCS_bg.mp4" type="video/mp4">-->
<!--              Your browser does not support the video tag.-->
<!--            </video>-->
<!--            <video ref="video2" controls @loadedmetadata="setVideoDimensions">-->
<!--              <source src="./video/UCCS_bg_enhance.mp4" type="video/mp4">-->
<!--              Your browser does not support the video tag.-->
<!--            </video>-->
<!--          </div>-->
<!--        </el-container>-->
<!--      </el-col>-->
<!--    </el-row>-->
<!--  </div>-->
<!--</template>-->

<!--<script>-->
<!--export default {-->
<!--  methods: {-->
<!--    setVideoDimensions() {-->
<!--      const video1 = this.$refs.video1;-->
<!--      const video2 = this.$refs.video2;-->

<!--      // 设置视频的高度和宽度-->
<!--      const height = Math.max(video1.videoHeight, video2.videoHeight);-->
<!--      const width = video1.videoWidth + video2.videoWidth;-->

<!--      video1.style.height = `${height}px`;-->
<!--      video2.style.height = `${height}px`;-->
<!--    }-->
<!--  }-->
<!--}-->
<!--</script>-->

<!--<style scoped>-->
<!--#video-container {-->
<!--  margin: 15px 0;-->
<!--}-->

<!--.video-wrapper {-->
<!--  display: flex;-->
<!--  justify-content: space-between;-->
<!--}-->

<!--video {-->
<!--  width: 50%; /* 每个视频占一半宽度 */-->
<!--  height: auto; /* 高度自动调整 */-->
<!--}-->
<!--</style>-->


<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Video Comparison</h1>
    </el-row>

    <!-- 左右并列播放视频 -->
    <el-row justify="center" gutter="20">
      <el-col :xs="24" :sm="12" :md="10" :lg="8" :xl="6">
        <el-container id="video-container-left">
          <video controls>
            <source src="/public/video/UCCS_bg.mp4" type="video/mp4" />
            Your browser does not support the video tag.
          </video>
        </el-container>
      </el-col>
      <el-col :xs="24" :sm="12" :md="10" :lg="8" :xl="6">
        <el-container id="video-container-right">
          <video controls>
            <source src="/public/video/UCCS_bg_enhance.mp4" type="video/mp4" />
            Your browser does not support the video tag.
          </video>
        </el-container>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>
.section-title {
  margin-bottom: 20px;
}

#video-container-left,
#video-container-right {
  margin: 15px 0px;
}

video {
  aspect-ratio: 16 / 9;
  width: 100%;
  height: auto;
}
</style>
