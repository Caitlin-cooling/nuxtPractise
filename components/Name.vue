<template>
  <div class="name">
    <p>The name field is active: {{ active }}</p>
    <label for="name">Name</label>
    <input 
      type="text"
      @focus="active=true"
    >
    <br />
    <button
      v-if="active"
      @click="active=false"
     >Confirm</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      active: false
    }
  },
}
</script>

<style scoped>
.name {
  padding: 20px;
}
</style>