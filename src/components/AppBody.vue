<template lang="html">
  <b-container class='bg-light' fluid>
    <b-row class="pt-3 justify-content-center">
      <Timeline />
      <SideContents />
    </b-row>
  </b-container>
</template>

<script>
import Timeline from '@/components/Timeline.vue'
import SideContents from '@/components/SideContents.vue'

export default {
  name: 'AppBody',
  components: {
    Timeline,
    SideContents
  }
}
</script>

<style lang="css" scoped>
</style>
