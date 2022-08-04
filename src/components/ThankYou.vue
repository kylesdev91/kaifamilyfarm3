<template>
  <div class="backdrop" @click="closeThankYou">
    <div class="modal" :class="{ sale: theme === 'sale' }">
      <h1>Thank you for your order!</h1>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    closeThankYou() {
      this.$emit('close');
    },
  },
};
</script>

<style>
.modal {
  width: 400px;
  padding: 20px;
  margin: 200px auto;
  background: white;
  border-radius: 10px;
}
.backdrop {
  top: 0;
  position: fixed;
  background: rgba(0, 0, 0, 0.5);
  width: 100%;
  height: 100%;
}
.modal h1 {
  color: black;
  border: none;
  padding: 0;
}
.modal p {
  font-style: normal;
}

/* sale styles */
.modal.sale {
  background: green;
  color: white;
}
.modal.sale h1 {
  color: white;
}
</style>
