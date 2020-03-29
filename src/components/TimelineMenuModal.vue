<template lang='html'>
  <vs-dialog not-close not-padding v-model='active'>
    <b-list-group class='text-center'>
      <b-list-group-item class='text-danger'>不適切な投稿を報告</b-list-group-item>
      <b-list-group-item class='text-danger'>フォローをやめる</b-list-group-item>
      <b-list-group-item>投稿へ移動</b-list-group-item>
      <b-list-group-item>シェア</b-list-group-item>
      <b-list-group-item>リンクをコピー</b-list-group-item>
      <b-list-group-item>埋め込み</b-list-group-item>
      <b-list-group-item>キャンセル</b-list-group-item>
    </b-list-group>
  </vs-dialog>
</template>

<script>
export default {
  name: 'TimelineMenuModal',
  props: {
    active: { type: Boolean, default: false },
    id: { tyoe: Number, required: true }
  }
}
</script>

<style lang="css" scoped>
</style>
