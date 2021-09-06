<template>
  <StartParts />
  <Nearby />
  <Docker />
</template>

<script>
import Docker from '../components/Docker'
import StartParts from '../components/StartParts'
import Nearby from '../components/Nearby'
export default {
  name: 'Home',
  components: { Docker, StartParts, Nearby }
}
</script>
<style>
</style>
