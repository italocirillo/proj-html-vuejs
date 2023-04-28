<script>
import CardPrezzi from './CardPrezzi.vue';
import Titolo from './Titolo.vue';


export default {
    name: "SezionePrezzi",
    components: { CardPrezzi, Titolo },
}
</script>

<template>
    <section class="sezione-prezzi py-3">
        <div class="container">
            <div class="intestazione py-3">
                <Titolo :titolo="'Our rates for developer from Landrick team'" class="p-1" />
            </div>
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
        <div class="intestazione intestazione-bottom">
            <Titolo :titolo="'Want to be among the first to find out?'" />
            <div class="input-group mb-3">
                <input type="email" class="form-control" placeholder="Email Address" aria-label="Email"
                    aria-describedby="basic-addon1">
                <span class="input-group-text" id="basic-addon1"><button class="bottone-pieno">Get Started</button></span>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.intestazione-bottom {
    width: 70%;
    margin: 0 auto;

    .input-group {
        width: 50%;
        margin: 0 auto;

        input {
            background-color: white;
            width: 60%;
            border: 1px solid $background-button;
            border-radius: 50px;
            padding: 0.8em;

            &.form-control {
                border-right: 0px;
                box-shadow: none;
            }
        }

        .input-group-text {
            background-color: white;
            border: 1px solid $background-button;
            border-radius: 50px;

            button {
                border-radius: 50px;
            }
        }
    }
}
</style>