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
            <div class="intestazione">
                <h2>Our rates for developer from landrick team</h2>
                <p>Start working with <span>Landrick</span>that can provide everything you need to
                    generate
                    awareness,drive
                    traffic, connect</p>
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
            <h2>Want to be among the first to find out?</h2>
            <p>Start working with <span>Landrick</span>that can provide everything you need to
                generate
                awareness,drive
                traffic, connect
            </p>
            <div class="input-group mb-3">
                <input type="email" class="form-control" placeholder="Email Address" aria-label="Email"
                    aria-describedby="basic-addon1">
                <span class="input-group-text" id="basic-addon1"><button class="bottone-pieno">Get Started</button></span>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.intestazione {
    text-align: center;
    width: 75%;
    margin: 0 auto;
    padding: 2em;

    h2 {
        font-weight: 600;
    }

    p {
        width: 75%;
        margin: 0 auto;
        font-weight: 700;
        padding: 1em 0em;

        span {
            color: $text-color-active;
        }
    }

    &.intestazione-bottom {
        padding: 5em 0em;
        width: 50%;

        p {
            width: 90%;
        }
    }

    .input-group {
        width: 80%;
        margin: 0 auto;

        input {
            background-color: white;
            width: 50%;
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