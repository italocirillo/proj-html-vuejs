<script>
import Jumbotron from './Jumbotron.vue';

export default {
    name: "AppMain",
    components: { Jumbotron },
    data() {
        return {
            affiliati: [
                {
                    url: "amazon.svg",
                    name: "amazon",
                },
                {
                    url: "google.svg",
                    name: "google",
                },
                {
                    url: "lenovo.svg",
                    name: "lenovo",
                },
                {
                    url: "paypal.svg",
                    name: "paypal",
                },
                {
                    url: "shopify.svg",
                    name: "shopify",
                },
                {
                    url: "spotify.svg",
                    name: "spotify",
                },
            ]
        }
    }
}
</script>

<template>
    <main>
        <Jumbotron :affiliati="affiliati" />
    </main>
</template>

<style lang="scss" scoped></style>