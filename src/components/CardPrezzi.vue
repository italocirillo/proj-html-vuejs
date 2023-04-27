<script>
import "@fortawesome/fontawesome-free/css/all.css";
export default {
    name: "CardPrezzi",
    props: {
        pianoAcquisto: String,
        prezzo: String,
        descrizione: String,
        nCard: Number,
    }
}
</script>

<template>
    <div class="card-prezzi">
        <div v-if="nCard === 2" class="fascia"><span>best</span></div>
        <span class="etichetta">{{ pianoAcquisto }}</span>
        <h2>{{ prezzo }}</h2>
        <p>Per Month</p>
        <p>{{ descrizione }}</p>
        <hr>
        <ul>
            <li><i class="fa-regular fa-circle-check"></i>Full Access</li>
            <li><i class="fa-regular fa-circle-check"></i>Enhanced Security</li>
            <li><i class="fa-regular fa-circle-check"></i>Source Files</li>
            <li><i class="fa-regular fa-circle-check"></i>1 Domain Free</li>
            <li><i class="fa-regular fa-circle-check"></i>Enhanced Security</li>
        </ul>
        <button class="bottone-pieno">Buy Now</button>
        <p>*No credit card requied</p>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.card-prezzi {
    background-color: white;
    border: 1px solid $background-button;
    padding: 1.5em;
    padding-bottom: 0.5em;
    border-radius: 10px;
    box-shadow: 0px 3px 0px gray;
    cursor: pointer;
    position: relative;

    .fascia {
        width: 65px;
        height: 65px;
        overflow: auto;
        position: absolute;
        top: -5px;
        right: -5px;

        span {
            position: absolute;
            display: block;
            width: 100px;
            background-color: #f17426;
            left: -12px;
            top: 20px;
            transform: rotate(45deg);
            color: #fff;
            font-weight: 900;
            font-size: 0.6rem;
            text-transform: uppercase;
            text-align: center;
        }

        &::before,
        &::after {
            border-top-color: transparent;
            border-right-color: transparent;
            position: absolute;
            z-index: -1;
            content: '';
            display: block;
            border: 2px solid #b1551c;
        }

        &::before {
            top: 0;
            left: 0px;
        }

        &::after {
            bottom: 0px;
            right: 0;
        }
    }

    .etichetta {
        background-color: $background-button;
        color: $text-color-active;
        padding: 1em 2em;
        border-radius: 20px;
        font-size: 0.8rem;
        font-weight: 800;
    }

    hr {
        color: $text-color-light;
    }

    h2 {
        padding-top: 0.5em;
        font-weight: 800;
    }

    p {
        font-weight: 700;
    }

    ul {
        padding: 0em;
        color: $text-color-light;
        font-weight: 700;

        li {
            padding: 0.4em 0em;
            font-weight: 800;

            i {
                font-size: 1.2rem;
                padding-right: 0.2em;
            }
        }
    }

    .bottone-pieno {
        width: 100%;
        margin-bottom: 1em;
    }

    &:hover {
        transform: scale(1.05);
        box-shadow: 0px 3px 0px $text-color-active;
    }
}
</style>