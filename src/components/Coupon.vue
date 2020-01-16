<template>
  <div>
    <label>
      <input type="text" placeholder="Enter your coupon code..." @blur="applyCoupon">
    </label>
  </div>
</template>

<script>
    export default {
        name: "Coupon",
        methods: {
            applyCoupon() {
              this.$emit('applied')
            }
        }
    }
</script>

<style scoped>
  input {
    font-size: 1em;
    font-weight: lighter;
    padding: 10px 5px
  }
</style>