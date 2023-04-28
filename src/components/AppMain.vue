<script>
import Jumbotron from './Jumbotron.vue';
import Features from './Features.vue';
import SezionePrezzi from './SezionePrezzi.vue';

export default {
    name: "AppMain",
    components: { Jumbotron, Features, SezionePrezzi, },
    props: {
        affiliati: Array,
    }
}
</script>

<template>
    <main>
        <Jumbotron :affiliati="affiliati" />
        <Features />
        <SezionePrezzi />
    </main>
</template>

<style lang="scss" scoped></style>