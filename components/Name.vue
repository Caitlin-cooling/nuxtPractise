<template>
  <div class="name">
    <p>The name field is active: {{ editing }}</p>
    <label for="name">Name</label>
    <input 
      type="text"
      @focus="handleEdit"
    >
    <br />
    <button
      v-if="editing"
      @click="cancelEdit"
     >Cancel</button>
    <button
      v-if="editing"
      @click="handleConfirm"
     >Confirm</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      editing: false
    }
  },
  methods: {
    handleEdit() {
      this.editing = true;
      document.querySelector('.name').classList.add('is-being-edited');
      const node = document.createElement('div');
      node.classList.add('edit-mask');
      document.querySelector('.container').appendChild(node);
    },
    cancelEdit() {
      this.editing = false;
      const node = document.querySelector('.edit-mask');
      document.querySelector('.container').removeChild(node);
    },
    handleConfirm() {
      this.editing = false;
      const node = document.querySelector('.edit-mask');
      document.querySelector('.container').removeChild(node);
    }
  }
}
</script>

<style>
.name {
  padding: 20px;
  width: 200px;
}

.is-being-edited {
  z-index: 10;
  position: absolute;
  background-color: white;
}

.edit-mask {
  height: 100%;
  width: 100%;
  top: 0;
  left: 0;
  background-color: grey;
  opacity: 0.5;
  position: absolute;
}
</style>