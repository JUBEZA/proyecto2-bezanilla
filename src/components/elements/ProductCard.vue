<template>
    <div class="card  mx-3 my-3 p-3" style="width: 18rem;background-color: rgb(160, 114, 114)">
        <img class="card-img-top" :src="producto.image" :alt="producto.name"
            style="object-fit: cover; width: 100%; aspect-ratio: 1/1;">>
        <div class="card-body">

            <p class="card-text text-light">{{ producto.name }}</p>
            <p class="card-text text-light">{{ producto.price }}</p>
            <button class="btn btn-light text-dark" @click="innerAddItemToCart"> Add to Cart</button>
        </div>
    </div>
</template>

<script>


export default {
    name: 'ProductCard',
    props: {
        producto:{
            type: Object,
            required: true

        },
        imageUrl: String,
        productName: String,
        productPrice: Number,
        productId: Number,


    },
    methods: {
        innerAddItemToCart(){
            this.$emit('addItem', this.producto);
            this.$store.dispatch('agregarItemACarrito',this.producto.id);
            this.$store.dispatch('actualizarCarritoUsuario');
        }
    }
}

</script>

<style scoped></style>
