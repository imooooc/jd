<template>
  <div>Hello, {{ name }}</div>
  <Friday msg="good job" />
</template>

<script>
import Friday from '../components/Fridy.vue'
export default {
  components: { Friday },
  name: 'Haha',
  data () {
    return {
      name: 'Jackie'
    }
  }
}
</script>

<style scoped>
body {
  background-color: red;
}
</style>
