<script>
import { defineComponent } from 'vue'
import { VideoPlayer } from '@videojs-player/vue'
import 'video.js/dist/video-js.css'

export default defineComponent({
  components: {
    VideoPlayer
  }
})
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Explainer Video</h1>
    </el-row>

    <!-- 每个网站的视频的iframe可能不一致，最好在这里手动调整 -->


    <!-- 本地视频 -->
    <el-row justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="10" >
        <el-container class="video-container">
          <video-player
            src="./video/UCCS_bg_enhance.mp4"
            controls
            fluid="true"
            muted="true"
            :volume="0.5"
          />
        </el-container>
      </el-col>
    </el-row>

  </div>
</template>

<style scoped>

.video-container{
  margin: 15px 0px 0px 0px;
}

iframe {
  aspect-ratio: 16 / 9;
  height: 100%;
  width: 100%;
}

</style>



<!--<script>-->



<!--export default {-->

<!--  data() {-->
<!--    return {-->

<!--      // 选择video-->
<!--      video_paths: [-->
<!--        "./video/UCCS_bg.mp4",-->
<!--        "./UCCS_bg.mp4",-->
<!--        "../../../../pubic/video/UCCS_bg.mp4",-->
<!--        "/public/video/UCCS_bg.mp4",-->


<!--      ],-->
<!--    }-->
<!--  }-->
<!--}-->

<!--</script>-->

<!--<template>-->

<!--&lt;!&ndash;  <div v-for="(videoPath, index) in video_paths" :key="index">&ndash;&gt;-->
<!--&lt;!&ndash;  <p>{{ videoPath }}</p>&ndash;&gt;-->
<!--&lt;!&ndash;  <video controls>&ndash;&gt;-->
<!--&lt;!&ndash;    <source :src="videoPath" type="video/mp4" />&ndash;&gt;-->
<!--&lt;!&ndash;  </video>&ndash;&gt;-->
<!--&lt;!&ndash;</div>&ndash;&gt;-->


<!--  <div>-->
<!--    <el-divider />-->

<!--    <el-row justify="center">-->
<!--      <h1 class="section-title">Video Comparison</h1>-->
<!--    </el-row>-->

<!--    &lt;!&ndash; 左右并列播放视频 &ndash;&gt;-->
<!--    <el-row justify="center" gutter="20">-->
<!--      <el-col-->
<!--        v-for="(videoPath, index) in video_paths"-->
<!--        :key="index"-->
<!--        :xs="24"-->
<!--        :sm="12"-->
<!--        :md="10"-->
<!--        :lg="8"-->
<!--        :xl="6"-->
<!--      >-->
<!--        <el-container :id="`video-container-${index}`">-->
<!--          <video controls>-->
<!--            <source :src="videoPath" type="video/mp4" />-->
<!--            Your browser does not support the video tag.-->
<!--          </video>-->
<!--        </el-container>-->
<!--      </el-col>-->
<!--    </el-row>-->
<!--  </div>-->
<!--</template>-->


<!--<style scoped>-->
<!--.section-title {-->
<!--  margin-bottom: 20px;-->
<!--}-->

<!--[id^="video-container"] {-->
<!--  margin: 15px 0px;-->
<!--}-->

<!--video {-->
<!--  aspect-ratio: 16 / 9;-->
<!--  width: 100%;-->
<!--  height: auto;-->
<!--}-->
<!--</style>-->

