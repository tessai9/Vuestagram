<template lang='html'>
  <TimelineCard
    :icon_img_path='icon_image_path'
    :posted_img_path='posted_image_path'
    display_user_name='test.user'
    description='This is my post.'
  />
</template>

<script>
import TimelineCard from '@/components/TimelineCard.vue'

const sample_icon_image = require('@/assets/logo.png')
const sample_posted_image = require('@/assets/kobe.jpg')

export default {
  name: 'Timeline',
  data() {
    return {
      icon_image_path: sample_icon_image,
      posted_image_path: sample_posted_image
    }
  },
  components: {
    TimelineCard
  }
}
</script>

<style lang="css" scoped>
.body-max-width {
  max-width: 935px;
}
.post-item-max-width {
  max-width: 614px;
}
</style>
