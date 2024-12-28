<script lang="ts" setup>
import { VueCompareImage } from 'vue3-compare-image';

const inputImagePath = './image_inner/1_gt.jpg';
const outputImagePath = './image_inner/1_input.png';

const inputImagePath2 = './image_inner/2_gt.png';
const outputImagePath2 = './image_inner/2_input.png';

const inputImagePath3 = './image_inner/3_gt.jpg';
const outputImagePath3 = './image_inner/3_input.png';

const inputImagePath4 = './image_inner/4_gt.jpg';
const outputImagePath4 = './image_inner/4_input.png';
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Image Inner Comparison</h1>
    </el-row>


     <el-row justify="center">
        <el-col :xs="12" :sm="10" :md="8" :lg="6" :xl="6">
            <el-row style="margin-top: 20px;" >
                <VueCompareImage
                    :left-image="inputImagePath"
                    :right-image="outputImagePath"
                    :hover="true"
                />
            </el-row>
        </el-col>
        <el-col :xs="12" :sm="10" :md="8" :lg="6" :xl="6">
            <el-row style="margin-top: 20px;" >
                <VueCompareImage
                    :left-image="inputImagePath2"
                    :right-image="outputImagePath2"
                    :hover="true"
                />
            </el-row>
        </el-col>
    </el-row>

     <el-row justify="center">
        <el-col :xs="12" :sm="10" :md="8" :lg="6" :xl="6">
            <el-row style="margin-top: 20px;" >
                <VueCompareImage
                    :left-image="inputImagePath3"
                    :right-image="outputImagePath3"
                    :hover="true"
                />
            </el-row>
        </el-col>
        <el-col :xs="12" :sm="10" :md="8" :lg="6" :xl="6">
            <el-row style="margin-top: 20px;" >
                <VueCompareImage
                    :left-image="inputImagePath4"
                    :right-image="outputImagePath4"
                    :hover="true"
                />
            </el-row>
        </el-col>
    </el-row>




  </div>






</template>

<style scoped>

</style>
