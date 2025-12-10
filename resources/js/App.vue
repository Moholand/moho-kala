<template>
    <Header v-if="['login', 'register'].indexOf($route['name']) === -1"/>
    <router-view></router-view>
    <Footer v-if="['login', 'register'].indexOf($route['name']) === -1"/>
</template>

<script>
import Header from "./components/home/Header.vue";
import Footer from "./components/home/Footer.vue";

export default {
    components: { Header, Footer },
}
</script>
