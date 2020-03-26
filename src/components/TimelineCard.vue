<template lang="html">
  <div>
    <b-card-group class='col-6 body-max-width mr-3'>
      <b-card body-class='p-0' class='post-item-max-width' header-bg-variant='white'>
        <div slot='header'>
          <vs-avatar history history-gradient circle size='30' class='d-inline-block align-middle'>
            <img v-if='icon_img_path' :src='icon_img_path' alt='' />
          </vs-avatar>
          <span class='align-middle ml-3'>{{ display_user_name }}</span>
          <box-icon name='dots-horizontal-rounded' class='float-right' @click="modal_active = !modal_active"></box-icon>
        </div>
        <div>
          <img :src='posted_img_path' alt='' class="w-100">
        </div>
        <b-card-text>
          <b-container class='px-3 pt-2'>
            <box-icon name='heart' size='md' class='mr-3'></box-icon>
            <box-icon name='message-rounded' size='md' class='mr-3'></box-icon>
            <box-icon name='navigation' size='md'></box-icon>
            <box-icon name='bookmark' size='md' class='float-right'></box-icon>
          </b-container>
          <b-container class='px-3 mt-0'>
            <b class='mr-1'>{{ display_user_name }}</b><span>{{ description }}</span>
          </b-container>
        </b-card-text>
      </b-card>
    </b-card-group>
    <ModalForPost :active="modal_active" />
  </div>
</template>

<script>
import ModalForPost from '@/components/ModalForPost.vue'

export default {
  name: 'TimelineCard',
  props: {
    icon_img_path: { type: String, default: '' },
    posted_img_path: { type: String, required: true },
    display_user_name: { type: String, default: '' },
    description: { type: String, default: '' }
  },
  data() {
    return {
      modal_active: false
    }
  },
  components: {
    ModalForPost
  }
}
</script>

<style lang="css" scoped>
</style>
