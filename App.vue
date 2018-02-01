<template>
  <Directory :directory="dir" />
</template>


<script>
import Directory from './Directory.vue'

export default {
  data: () => ({
dir: {
name: 'one',
children: [
{ name: '1' },
{ name: '2', children: [
{ name: 'III', children: [
{ name: '1' },
{ name: '2', children: [
{ name: 'III' }
] }
] }
] }
]
}
}),
  components: { Directory }
}
</script>
