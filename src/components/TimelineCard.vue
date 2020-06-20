<template lang='html'>
  <b-card body-class='p-0' class='post-item-max-width' header-bg-variant='white' footer-bg-variant='white'>
    <div slot='header'>
      <vs-avatar history history-gradient circle size='30' class='d-inline-block align-middle'>
        <img v-if='icon_img_path' :src='icon_img_path' alt='' />
      </vs-avatar>
      <span class='align-middle ml-3'>{{ display_user_name }}</span>
      <box-icon name='dots-horizontal-rounded' class='float-right card-menu' @click='openPostMenu'></box-icon>
    </div>
    <div>
      <img :src='posted_img_path' alt='' class='w-100'>
    </div>
    <b-card-text>
      <b-container class='px-3 pt-2'>
        <box-icon name='heart' size='md' class='mr-3'></box-icon>
        <box-icon name='message-rounded' size='md' class='mr-3'></box-icon>
        <box-icon name='navigation' size='md'></box-icon>
        <box-icon name='bookmark' size='md' class='float-right'></box-icon>
      </b-container>
      <b-container class='px-3 mt-0'>
        <b class='mr-1'>{{ display_user_name }}</b>
        <span>{{ description }}</span>
      </b-container>
    </b-card-text>
    <div slot='footer' class='post-comment-area text-center'>
      <b-row no-gutters=true align-v='center'>
        <b-col class='px-0' cols='9'>
          <vs-input type='text' label-placeholder='コメントを追加...' v-model='comment' />
        </b-col>
        <b-col class='text-primary'>
          <a href='#' class='comment-text-size'>投稿する</a>
        </b-col>
      </b-row>
    </div>
  </b-card>
</template>

<script>
export default {
  name: 'TimelineCard',
  props: {
    post_id: { type: Number, required: true },
    icon_img_path: { type: String, default: '' },
    posted_img_path: { type: String, required: true },
    display_user_name: { type: String, default: '' },
    description: { type: String, default: '' }
  },
  data() {
    return {
      comment: ''
    }
  },
  methods: {
    openPostMenu() {
      this.$emit('open-menu', this.post_id)
    }
  },
}
</script>

<style lang="css" scoped>
.body-max-width {
  max-width: 935px;
}
.post-item-max-width {
  max-width: 614px;
}
.post-comment-area {
  height: 2.5rem;
  align-items: center;
  padding: 0;
}
.comment-text-size {
  font-size: 0.8rem;
}
.card-menu {
  cursor: pointer;
}
</style>
