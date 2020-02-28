<template>
  <div>
    <p>The name field is active: {{ active }}</p>
    <label for="name">Name</label>
    <input 
      type="text"
      id="name"
      name="name"
      @focus="active=true"
      @blur="active=false"
    >
    <!-- what about when the button is active? -->
    <button v-if="active">Confirm</button>
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