<script>

export default {
  data() {
    return {
      abstract: " This is abstract about W2WDiff"
    }
  }
}
</script>

<template>
  <div>
    <el-divider />

    <el-row justify="center">
      <h1 class="section-title">Abstract</h1>
    </el-row>

    <el-row justify="center">
      <el-col :xs="24" :sm="20" :md="16" :lg="12" :xl="12">
        <p>{{ abstract }}</p>
      </el-col>
    </el-row>
  </div>
</template>

<style scoped>

/* 摘要文字居中 */
p {
  text-align: justify;
} 

</style>