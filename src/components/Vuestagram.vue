<template lang="html">
  <div>
    <AppNavBar />
    <AppBody />
  </div>
</template>

<script>
import AppNavBar from '@/components/AppNavBar.vue'
import AppBody from '@/components/AppBody.vue'

export default {
  name: 'Vuestagram',
  components: {
    AppNavBar,
    AppBody
  }
}
</script>

<style lang="css" scoped>
</style>
