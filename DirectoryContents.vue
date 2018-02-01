<template>  
  <ul>
    <li v-for="directory in children" :key="directory.name">
      <directory v-if="directory.children" :directory="directory"></directory>
      <span v-else>{{ directory.name }}</span>
    </li>
  </ul>
</template>

<script>
// import Directory from './Directory.vue'
const Directory = () => import('./Directory.vue')

export default {
  name: 'DirectoryContents',
  props: ['children'],
  components: {
    Directory
  }
}
</script>

