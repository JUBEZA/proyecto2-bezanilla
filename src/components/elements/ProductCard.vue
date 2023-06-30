<template>
  <div class="card  mx-3 my-3 p-3" style="background-color: darkgreen;width: 18rem;">
      <img class="card-img-top" :src="productoObjeto.image" :alt="productoObjeto.name"
          style="object-fit: cover; width: 100%; aspect-ratio: 1/1;">>
      <div class="card-body">

          <p class="card-text text-light" >{{ productoObjeto.name }}</p>
          <p class="card-text text-light">{{ productoObjeto.price }}</p>
          <button class="btn btn-light text-dark" @click="innerAddItemToCart"> Add to Cart</button>
      </div>
  </div>
</template>

<script>


export default {
  name: 'ProductCard',
  props: {
      // imageUrl: String,
      // productName: String,
      // productPrice: Number,
      // productId: Number,
      productoObjeto: {}


  },
  methods: {
      innerAddItemToCart(){
          this.$emit('addItem', this.productoObjeto.id);
      }
  }
}

</script>

<style scoped></style>
