<script>
import Jumbotron from './Jumbotron.vue';
import SezionePrezzi from './SezionePrezzi.vue';

export default {
    name: "AppMain",
    components: { Jumbotron, SezionePrezzi },
    props: {
        affiliati: Array,
    }
}
</script>

<template>
    <main>
        <Jumbotron :affiliati="affiliati" />
        <SezionePrezzi />
    </main>
</template>

<style lang="scss" scoped></style>