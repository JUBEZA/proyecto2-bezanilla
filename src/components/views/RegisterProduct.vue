<template>
    <div>
        <HeaderSite :inventario="this.$store.state.inventario"/>
        <FormularioProducto />
    </div>
  </template>

<script>
// import LoginSite from '../elements/LoginSite.vue'
import FormularioProducto from '../elements/FormularioProducto.vue';
import HeaderSite from '../elements/HeaderSite.vue';


export default {
    name: 'RegisterProduct',
    props: {

    },
    components: {
    HeaderSite,
    FormularioProducto,

}
}

</script>

<style scoped></style>
