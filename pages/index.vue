<template>
  <div class="container">
    <nuxt-link to="/users">Click for users</nuxt-link><br/>
    <nuxt-link to="/products">Click for products</nuxt-link>
    <Name />
  </div>
</template>

<script>
import Name from '~/components/Name'
export default {
  components: { Name }
}
</script>

<style scoped>
.container {
  padding: 20px;
}
</style>

