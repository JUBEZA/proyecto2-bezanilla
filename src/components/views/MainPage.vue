<template>
  <div>

      <h1 class="text-white p-5 m-5 fw-bold" style="background-image: url(https://www.turismobr.com/wp-content/uploads/2011/03/Bandera-de-Brasil.png); background-size: cover; background-position: center; -webkit-text-stroke-width: 1px; -webkit-text-stroke-color: black;">¡¡Los mejores destinos de brazil te esperan!!</h1>
      <div class="row justify-content-around mx-4">
          <ProductCard v-for="(item, i) in inventario" :key="i" :productoObjeto="item" @addItem="handleAddItem" />

      </div>
  </div>
</template>

<script>
import ProductCard from '../elements/ProductCard.vue'


export default {
  name: 'MainPage',
  props: {
      inventario: {
          type: Array,
          required: true
      }

  },

  components: {
      ProductCard,

  },
  methods: {
      handleAddItem(productId) {
          this.$emit('itemAdded', productId);
      },
  },
}

</script>


<style scoped></style>
