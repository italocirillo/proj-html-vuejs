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
                    <CardPrezzi :pianoAcquisto="'Basic'" :prezzo="'9.00$'"
                        :descrizione="'All the basic for business that are just getting started'" :nCard="1" />
                </div>
                <div class="col">
                    <CardPrezzi :pianoAcquisto="'Business'" :prezzo="'39.00$'"
                        :descrizione="'Better for growing businesses that want more customers'" :nCard="2" />
                </div>
                <div class="col">
                    <CardPrezzi :pianoAcquisto="'Enterprise'" :prezzo="'79.00$'"
                        :descrizione="'Advanced features for pros who need more customization'" :nCard="3" />
                </div>
            </div>
        </div>

    </div>
</template>

<style lang="scss" scoped></style>