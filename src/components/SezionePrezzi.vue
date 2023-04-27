<script>
import CardPrezzi from './CardPrezzi.vue';


export default {
    name: "SezionePrezzi",
    components: { CardPrezzi },
}
</script>

<template>
    <div class="sezione-prezzi py-3">
        <div class="container">
            <div class="row">
                <div class="col">
                    <CardPrezzi />
                </div>
                <div class="col">
                    <CardPrezzi />
                </div>
                <div class="col">
                    <CardPrezzi />
                </div>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped></style>