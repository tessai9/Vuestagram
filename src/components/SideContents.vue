<template lang="html">
  <div class='col-3'>
    <vs-avatar history history-gradient circle size='50' class='d-inline-block align-middle'>
      <img :src='sample_img_path' alt=''>
    </vs-avatar>
    <div class='d-inline-block align-middle ml-3 user-name-text-size'>
      <b>tettyanman99</b><br />
      てっちゃん
    </div>
    <div class='mt-3'>
      <SideContentCard
        header_title='ストーリーズ'
        :icon_img_path='sample_img_path'
        user_name='test.user'
        sub_information='16時間前'
        contents_type='stories'
      />
      <SideContentCard
        class='mt-2'
        header_title='おすすめ'
        :icon_img_path='sample_img_path'
        user_name='test.user'
        sub_information='test.userがフォロー中'
        contents_type='recommend_users'
      />
    </div>
  </div>
</template>

<script>
import SideContentCard from '@/components/SideContentCard.vue'

const sample_image = require('@/assets/logo.png')

export default {
  name: 'SideContents',
  data() {
    return {
      sample_img_path: sample_image
    }
  },
  components: {
    SideContentCard
  }
}
</script>

<style lang="css" scoped>
.stories_card_height {
  height: 182px;
}
.user-name-text-size {
  font-size: 0.8rem;
}
.addtionalInfo-text-size {
  font-size: 0.6rem;
}
.follow-action-text-size,
.see-all-text-size {
  font-size: 0.8rem;
}
.side-contents-title-text-size {
  font-size: 0.9rem;
}
</style>
