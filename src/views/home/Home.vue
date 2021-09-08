<template>
  <StartParts />
  <Nearby />
  <Docker />
</template>

<script>
import Docker from './Docker'
import StartParts from './StartParts'
import Nearby from './Nearby'
export default {
  name: 'Home',
  components: { Docker, StartParts, Nearby }
}
</script>
<style lang="scss">
@import '../../css/index.scss';
</style>
