<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Markdown from './sections/Markdown.vue'
import Echart from './sections/Echart.vue'
import Carousel from './sections/Carousel.vue'
import Table from './sections/Table.vue'


export default {
  components: {
    Title,
    Abstract,
    Markdown,
    Echart,
    Table,
    BibTeX
  }
}
</script>

<template>
  <Title/>
  <Abstract/>
  <Markdown/>
  <Echart/>
  <Table/>
</template>
