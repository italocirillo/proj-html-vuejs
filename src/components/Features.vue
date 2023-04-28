<script>
import Titolo from "./Titolo.vue";
import CardFeatures from "./CardFeatures.vue"
export default {
    name: "Features",
    components: { Titolo, CardFeatures },
    data() {
        return {
            carte: [
                {
                    indirizzoIcona: "../../node_modules/@fortawesome/fontawesome-free/svgs/solid/layer-group.svg",
                    titolo: "Modular"
                },
                {
                    indirizzoIcona: "../../node_modules/@fortawesome/fontawesome-free/svgs/solid/laptop.svg",
                    titolo: "Responsive"
                },
                {
                    indirizzoIcona: "../../node_modules/@fortawesome/fontawesome-free/svgs/solid/circle-nodes.svg",
                    titolo: "Customizable"
                },
                {
                    indirizzoIcona: "../../node_modules/@fortawesome/fontawesome-free/svgs/solid/maximize.svg",
                    titolo: "Scalable"
                }
            ]
        }
    }
}
</script>

<template>
    <section class="features">
        <div class="container">
            <Titolo class="text-start m-0" :titolo="'Key Features'" />
            <div class="row row-col-4 align-items-start">
                <div class="col" v-for="(elemento, index) in carte" :key="index">
                    <CardFeatures :titolo="elemento.titolo" :indirizzoIcona="elemento.indirizzoIcona" />
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.row {
    .col {
        padding: 0;
        padding-left: 1em;
    }
}
</style>