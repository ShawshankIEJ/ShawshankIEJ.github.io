<script>
import Evaluation from './sections/Evaluation.vue'
import Video from './sections/Video.vue'
import Abstract from './sections/Abstract.vue'
import Markdown from './sections/Markdown.vue'
import Framework from './sections/Framework.vue'
import Bench from './sections/Bench.vue'
import Ethics from './sections/Ethics.vue'


export default {
  components: {
    Title,
    Abstract,
    Markdown,
    Evaluation,
    Bench,
    Framework,
    Ethics
  }
}
</script>

<template>
  <Title/>
  <Abstract/>
  <Markdown/>
  <Framework/>
  <Bench/>
  <Evaluation/>
  <Ethics/>
</template>
