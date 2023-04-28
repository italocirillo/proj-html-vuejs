<script>
import Jumbotron from './Jumbotron.vue';
import Features from './Features.vue';
import SezionePrezzi from './SezionePrezzi.vue';
import BuildTools from './BuildTools.vue';

export default {
    name: "AppMain",
    components: { Jumbotron, Features, SezionePrezzi, BuildTools },
    props: {
        affiliati: Array,
    }
}
</script>

<template>
    <main>
        <Jumbotron :affiliati="affiliati" />
        <Features />
        <BuildTools />
        <SezionePrezzi />
    </main>
</template>

<style lang="scss" scoped></style>