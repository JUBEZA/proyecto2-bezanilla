<template>
    <div class="card bg-transparent" style="width: 60rem;">

        <div class="row ">

            <p class="card-text text-light col-5">{{ producto.name }}</p>
            <p class="card-text text-light col-3">{{ producto.price }}</p>
            <p class="card-text text-light col-3">1</p>
            <button class="btn btn-light text-dark col-1" @click="removeFromCart"> Delete</button>
        </div>
    </div>
</template>

<script>


export default {
    name: 'CartCard',
    props: {
        producto: {
            type: Object,
            required: true
        },
        id: {
            type: Number,
            required: true
        },


    },
    methods: {
        removeFromCart() {
            console.log("Remove Item desde cartCard");
            console.log(this.id);
            this.$store.dispatch('eliminarItemCarrito', this.id)
            this.$store.dispatch('actualizarCarritoUsuario')

        },
        fetchData() {
            fetch("https://649eff62245f077f3e9d3860.mockapi.io/cities/cities")
                .then(response => response.json())
                .then(datos => {
                    // Aquí puedes trabajar con los datos obtenidos
                    console.log(datos);
                })

        }
    }
}

</script>

<style scoped></style>
