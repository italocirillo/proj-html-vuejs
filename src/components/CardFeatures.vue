<script>
import "@fortawesome/fontawesome-free/css/all.css";
export default {
    name: "CardFeatures",
    data() {
        return {
            cardHover: false,
        }
    },
    props: {
        indirizzoIcona: String,
        titolo: String,
    }
}
</script>

<template>
    <div class="card" @mouseenter="cardHover = true" @mouseleave="cardHover = false">
        <div class="card-hover" v-if="cardHover === true">
            <img :src="indirizzoIcona" :alt="indirizzoIcona">
        </div>
        <div class="quadratino">
            <img class="icona" :src="indirizzoIcona" :alt="indirizzoIcona">
        </div>
        <h2>{{ titolo }}</h2>
        <p>Composed in a pseudo-Latin language witch more or less corresponds.</p>
        <button class="bottone-vuoto"><a href="#">Read More <i class="fa-solid fa-chevron-right"></i></a></button>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.card {
    padding: 1em;
    border: 1px solid $background-button;
    cursor: pointer;
    position: relative;
    background-color: transparent;

    .quadratino {
        background-color: #eaeefb;
        width: 4rem;
        height: 4rem;
        display: flex;
        align-items: center;
        justify-content: center;
        border-radius: 5px;

        .icona {
            width: 50%;
            filter: invert(27%) sepia(56%) saturate(2525%) hue-rotate(215deg) brightness(92%) contrast(95%);

        }
    }

    h2 {
        font-size: 1rem;
        font-weight: 700;
        margin: 0;
        padding: 2em 0em 0.5em;
    }

    p {
        font-weight: 500;
        margin: 0;
        padding: 0.5em 0em;
    }

    .bottone-vuoto {
        width: 50%;
        padding-left: 0em;
        border: none;
        box-shadow: none;
        text-align: start;

        a,
        i {
            font-size: 0.8rem;
        }

        &:hover {
            padding-left: 1em;
            background-color: $text-color-active;
            box-shadow: 4px 4px 10px black;

            a,
            i {
                color: white;
            }
        }
    }

    .card-hover {
        position: absolute;
        width: 90%;
        z-index: -1;
        top: 1em;
        right: 1em;

        img {
            filter: opacity(0.1) invert(49%) sepia(0%) saturate(3106%) hue-rotate(150deg) brightness(104%) contrast(83%);
        }
    }

    // &:hover {
    //     fill-opacity: 0.4;
    //     background-color: none;
    //     background-image: url("../../node_modules/@fortawesome/fontawesome-free/svgs/solid/layer-group.svg");
    //     background-repeat: no-repeat;
    //     background-position: center center;
    // }

}
</style>