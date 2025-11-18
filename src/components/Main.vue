<script>
import Title from './sections/Title.vue'
import Abstract from './sections/Abstract.vue'
import Markdown from './sections/Markdown.vue'
import Carousel from './sections/Carousel.vue'
import Table from './sections/Table.vue'


export default {
  components: {
    Title,
    Abstract,
    Markdown,
    Table
  }
}
</script>

<template>
  <Title/>
  <Abstract/>
  <Markdown/>
  <Table/>
</template>
