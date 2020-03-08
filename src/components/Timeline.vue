<template lang='html'>
  <b-card-group class='col-6 body-max-width mr-3'>
    <b-card body-class='p-0' class='post-item-max-width' header-bg-variant='white'>
      <div slot='header'>
        <vs-avatar history history-gradient circle size='30' class='d-inline-block align-middle'>
          <img src='../assets/logo.png' alt=''>
        </vs-avatar>
        <span class='align-middle ml-3'>test.user</span>
        <box-icon name='dots-horizontal-rounded' class='float-right'></box-icon>
      </div>
      <div>
        <img src='../assets/kobe.jpg' alt='' class="w-100">
      </div>
      <b-card-text>
        <b-container class='px-3 pt-2'>
          <box-icon name='heart' size='md' class='mr-3'></box-icon>
          <box-icon name='message-rounded' size='md' class='mr-3'></box-icon>
          <box-icon name='navigation' size='md'></box-icon>
          <box-icon name='bookmark' size='md' class='float-right'></box-icon>
        </b-container>
        <b-container class='px-3 mt-0'>
          <b class='mr-1'>test.user</b><span>this is my post</span>
        </b-container>
      </b-card-text>
    </b-card>
  </b-card-group>
</template>

<script>
export default {
  name: 'Timeline'
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
