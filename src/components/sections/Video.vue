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
<!--          <iframe src="./UCCS_bg.mp4" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"></iframe>-->
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




<script>



export default {

  data() {
    return {

      // 选择video
      video_paths: [
        "./video/UCCS_bg.mp4",
        "./UCCS_bg.mp4",
        "../../../../pubic/video/UCCS_bg.mp4",
        "/public/video/UCCS_bg.mp4",


      ],
    }
  }
}

</script>

<template>

<!--  <div v-for="(videoPath, index) in video_paths" :key="index">-->
<!--  <p>{{ videoPath }}</p>-->
<!--  <video controls>-->
<!--    <source :src="videoPath" type="video/mp4" />-->
<!--  </video>-->
<!--</div>-->


  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Video Comparison</h1>
    </el-row>

    <!-- 左右并列播放视频 -->
    <el-row justify="center" gutter="20">
      <el-col
        v-for="(videoPath, index) in video_paths"
        :key="index"
        :xs="24"
        :sm="12"
        :md="10"
        :lg="8"
        :xl="6"
      >
        <el-container :id="`video-container-${index}`">
          <video controls>
            <source :src="videoPath" type="video/mp4" />
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

[id^="video-container"] {
  margin: 15px 0px;
}

video {
  aspect-ratio: 16 / 9;
  width: 100%;
  height: auto;
}
</style>

