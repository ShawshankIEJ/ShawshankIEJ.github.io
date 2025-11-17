<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Markdown from './sections/Markdown.vue'
import BibTeX from './sections/BibTeX.vue'
import Carousel from './sections/Carousel.vue'
import Table from './sections/Table.vue'


export default {
  components: {
    Title,
    Abstract,
    Markdown,
    Table,
    BibTeX
  }
}
</script>

<template>
  <Title/>
  <Abstract/>
  <Markdown/>
  <Table/>
</template>
