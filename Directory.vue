<template>
  <p>
    <span>{{ directory.name }}</span>
    <DirectoryContents :children="directory.children"/>
  </p>
</template>

<script>
import DirectoryContents from './DirectoryContents.vue'

export default {
  name: 'Directory',
  props: ['directory'],
  components: {
    DirectoryContents
  }
}
</script>
