<template lang='html'>
  <b-card-group class='col-6 body-max-width mr-3'>
    <TimelineCard
      v-on:open-menu='openDialog'
      :post_id='1'
      :icon_img_path='icon_image_path'
      :posted_img_path='posted_image_path'
      display_user_name='test.user'
      description='This is my post.'
    />
    <TimelineMenuModal :active='modal_active' :id='modal_target_id' />
  </b-card-group>
</template>

<script>
import TimelineCard from '@/components/TimelineCard.vue'
import TimelineMenuModal from '@/components/TimelineMenuModal.vue'

const sample_icon_image = require('@/assets/logo.png')
const sample_posted_image = require('@/assets/kobe.jpg')

export default {
  name: 'Timeline',
  data() {
    return {
      icon_image_path: sample_icon_image,
      posted_image_path: sample_posted_image,
      modal_active: false,
      modal_target_id: 1
    }
  },
  methods: {
    openDialog(post_id) {
      this.modal_target_id = post_id
      this.modal_active = !this.modal_active
    }
  },
  components: {
    TimelineCard,
    TimelineMenuModal
  }
}
</script>

<style lang="css" scoped>
</style>
