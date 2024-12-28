<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import BibTeX from './sections/BibTeX.vue'
import Carousel from './sections/Carousel.vue'
import Video from './sections/Video.vue'
import ImageSlider from './sections/ImageSlider.vue'
import ImageSliderInner from './sections/ImageSliderInner.vue'
import Echart from './sections/Echart.vue'
import Table from './sections/Table.vue'
import Collapse from './sections/Collapse.vue'
import SeletionForComparison from './sections/SeletionForComparison.vue'
import Comment from './sections/Comment.vue'
import Latex from './sections/Latex.vue'
import Model3D from './sections/Model3D.vue'
import GaussianSplats3D from './sections/GaussianSplats3D.vue'

export default {
  components: {
    Title,
    Abstract, //摘要
    BibTeX,
    Carousel, //图片轮播
    // Video,
    ImageSlider, //适合uccs那个
    ImageSliderInner, //一幅图可以拖拽那个
    // Echart,
    // Collapse,
    Table, //可以做个表格
    // SeletionForComparison,
    // Comment,
    // Latex,
    // Model3D,
    // GaussianSplats3D
  }
}
</script>

<template>
  <Title/>
  <Carousel/>
  <Video/>
  <Abstract/>
  <Latex/>
  <Table/>
  <Collapse/>
  <Echart/>
  <Model3D/>
  <GaussianSplats3D/>
  <SeletionForComparison/>
  <ImageSliderInner/>
  <ImageSlider/>
  <BibTeX/>
  <Comment/>
</template>