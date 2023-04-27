<script>
import "@fortawesome/fontawesome-free/css/all.css";
export default {
    name: "Jumbotron",
    props: {
        affiliati: Array,
    },
    methods: {
        getImagePath(image) {
            return new URL(`../assets/img/${image}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <div class="jumbotron">
        <button class="ingranaggio">
            <i class="fa-solid fa-gear"></i>
        </button>
        <div class="container">
            <div class="row align-items-start">
                <div class="col">
                    <div class="info">
                        <span class="etichetta">
                            Development
                        </span>
                        <h1>A Complete Developer Toolset</h1>
                        <p>Launch your campaign and benedit from our expertise on designing and managing conversion centered
                            bootstrap4 html page.
                        </p>
                        <button class="bottone-pieno me-3">
                            Get Started
                        </button>
                        <button class="bottone-vuoto">
                            Documentation
                        </button>
                        <p>Current Version v2.6.0</p>
                    </div>
                </div>
                <div class="col">
                    <img src="../assets/img/about.png" alt="jumbo-image">
                </div>
            </div>
        </div>
        <hr>
        <div class="container">
            <ul class="affiliati">
                <li v-for="(elemento, index) in affiliati" :key="index">
                    <img :src="getImagePath(elemento.url)" :alt="elemento.name">
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.jumbotron {
    background-color: $background;

    .ingranaggio {
        margin-top: 8em;
        padding: 0.5em 0.5em 0.5em 1em;
        border-radius: 0px 50px 50px 0px;
        background-color: white;
        color: $text-color-active;

        &:hover {
            background-color: $text-color-active;
            color: white;
        }
    }

    .container {

        img {
            width: 90%;
        }

        .info {
            padding: 4em 0em;

            .etichetta {
                background-color: $background-button;
                color: $text-color-active;
                padding: 0.3em 1em;
                border-radius: 20px;
                font-size: 0.7rem;
                font-weight: 600;
            }

            h1 {
                font-size: 3em;
                font-weight: 800;
                padding: 0.2em 0em;
            }

            p {
                font-weight: 700;
                padding: 1.2em 0em;
            }
        }

        .affiliati {
            display: flex;

            img {
                width: 40%;
                padding: 1em 0em;
            }
        }

    }
}
</style>