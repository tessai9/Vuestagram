<template lang='html'>
  <b-navbar variant="white" class="border-bottom px-5" sticky=true>
    <b-navbar-brand href="#">Vuestagram</b-navbar-brand>
    <!-- Right aligned nav items -->
    <b-navbar-nav class="ml-auto">
      <b-nav-text>
        <box-icon type='solid' name='home' size='sm' class='mr-3'></box-icon>
        <box-icon name='compass' size='sm' class='mr-3'></box-icon>
        <box-icon name='heart' size='sm' class='mr-3'></box-icon>
      </b-nav-text>
    </b-navbar-nav>
    <vs-avatar history history-gradient circle size='30'>
      <img src="@/assets/logo.png" alt="">
    </vs-avatar>
  </b-navbar>
</template>

<script>
import 'boxicons'

export default {
  name: 'AppNavBar'
}
</script>

<style lang="css" scoped>
</style>
