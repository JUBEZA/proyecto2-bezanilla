<template>
    <div>
        <HeaderSite :inventario="this.$store.state.inventario"/>
        <LoginSite />
      </div>
    </template>

<script>
import LoginSite from '../elements/LoginSite.vue'
import HeaderSite from '../elements/HeaderSite.vue';


export default {
    name: 'LoginPage',
    props: {

    },
    components: {
    LoginSite,
    HeaderSite,
}
}

</script>

<style scoped></style>
