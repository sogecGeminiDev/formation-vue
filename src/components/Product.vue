<template>
  <div class="product">
  </div>
</template>

<script>
export default {
  name: 'product',
  props: {
    url: {
      type:String,
      required: true
    },
    title: {
      type:String,
      required: true
    },
    price: {
      type: Number,
      required: true
    },
    description: {
      type:String,
      required: true
    }
  },
  methods: {
  }
}
</script>

<style scoped lang="scss">
.product {
  border: 1px solid #42b983;
  padding: 10px;
  border-radius: 5px;
  margin: 5px 0;
}
</style>