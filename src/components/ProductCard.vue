<template lang="pug">
b-card.card-product(img-top :img-src='product.image')
  b-card-body
    b-card-title
      router-link(:to='"/product/" + product._id') {{ product.name }}
    b-card-sub-title {{ product.category }} - {{ '$' + product.price }}
    b-card-text {{ product.description }}
</template>

<script>
export default {
  props: {
    product: {
      type: Object,
      require: true
    }
  }
}
</script>
