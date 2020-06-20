<template lang="html">
  <b-card
    body-class='p-2'
    header-class='px-3 py-2'
    header-bg-variant='white'
    header-border-variant='light'
  >
    <!-- header of card -->
    <div slot='header'>
      <b
        class='text-secondary
        side-contents-title-text-size'
      >
        {{ header_title }}
      </b>
      <span class='float-right see-all-text-size'>
        <b>すべて見る</b>
      </span>
    </div>
    <!-- body of card -->
    <div class='text-left stories_card_height'>
      <div>
        <!-- user list -->
        <vs-avatar
          history
          history-gradient
          circle
          size='40'
          class='d-inline-block align-middle'
        >
          <img v-if='icon_img_path' :src='icon_img_path' alt='' />
          <i v-else class='bx bx-user'></i>
        </vs-avatar>
        <div class='d-inline-block ml-2 align-middle user-name-text-size'>
          <b>{{ user_name }}</b>
          <br />
          <span class='text-secondaty addtionalInfo-text-size'>
            {{ sub_information }}
          </span>
        </div>
        <div v-if='contents_type == "recommend_users"' class='d-inline-block ml-4'>
          <b class='text-primary follow-action-text-size align-middle'>フォローする</b>
        </div>
      </div>
    </div>
  </b-card>
</template>

<script>
export default {
  name: 'SideContentCard',
  props: {
    header_title: { type: String, default: '' },
    icon_img_path: { type: String, default: '' },
    user_name: { type: String, default: '' },
    sub_information: { type: String, default: '' },
    contents_type: { type: String, default: '' }
  }
}
</script>

<style lang="css" scoped>
.stories_card_height {
  height: 182px;
}
.user-name-text-size,
.follow-action-text-size,
.see-all-text-size {
  font-size: 0.8rem;
}
.addtionalInfo-text-size {
  font-size: 0.6rem;
}
.side-contents-title-text-size {
  font-size: 0.9rem;
}
</style>
