<template>
    <div>
        <HeaderSite :inventario="this.$store.state.inventario"/>
        <FormularioRegistro />
    </div>
  </template>

<script>
// import LoginSite from '../elements/LoginSite.vue'
import FormularioRegistro from '../elements/FormularioRegistro.vue';
import HeaderSite from '../elements/HeaderSite.vue';


export default {
    name: 'RegisterPage',
    props: {

    },
    components: {
    FormularioRegistro,
    HeaderSite,
}
}

</script>

<style scoped></style>
