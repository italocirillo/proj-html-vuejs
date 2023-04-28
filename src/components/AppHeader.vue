<script>
import "@fortawesome/fontawesome-free/css/all.css";
export default {
    name: "AppHeader",
    props: {
        arrayHeader: Array,
    },
    data() {
        return {
            elementoAttivo: 1,
            search: false,
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <div class="row align-items-center">
                <!-- Logo -->
                <div class="col-3">
                    <a href="#"><img class="logo" src="../assets/img/logo-dark.png" alt="logo"></a>
                </div>
                <!-- NavBar Props -->
                <div class="col-6">
                    <nav class="navbar navbar-expand-lg bg-body-tertiary">
                        <div class="container-fluid">
                            <div class="collapse navbar-collapse justify-content-center" id="navbarNav">
                                <ul class="navbar-nav">
                                    <li class="nav-item" v-for="(elemento, index) in arrayHeader"
                                        @click="elementoAttivo = index" :key="index">
                                        <a class="nav-link props" href="#"
                                            :class="index === elementoAttivo ? 'active' : ''">{{
                                                elemento }}
                                            <span v-if="index > 0">
                                                <i class="fa-solid fa-chevron-down"></i>
                                            </span>
                                        </a>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </nav>
                </div>
                <!-- NavBar Icone -->
                <div class="col-3">
                    <nav class="navbar navbar-expand-lg bg-body-tertiary">
                        <div class="container-fluid">
                            <button class="navbar-toggler" type="button" data-bs-toggle="collapse"
                                data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false"
                                aria-label="Toggle navigation">
                                <span class="navbar-toggler-icon"></span>
                            </button>
                            <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
                                <ul class="navbar-nav">
                                    <li class="nav-item d-flex align-items-center gap-2">
                                        <input v-if="search === true" type="search" class="rounded w-100"
                                            placeholder="Ricerca" aria-label="Search" aria-describedby="search-addon" />
                                        <i class="fa-solid fa-magnifying-glass" @click="search = !search"></i>
                                    </li>
                                    <li class="nav-item">
                                        <button class="bottoni-icone">
                                            <a class="nav-link" href="#">
                                                <i class="fa-brands fa-github"></i>
                                            </a>
                                        </button>
                                    </li>
                                    <li class="nav-item">
                                        <button class="bottoni-icone">
                                            <a class="nav-link" href="#">
                                                <i class="fa-brands fa-stack-overflow"></i>
                                            </a>
                                        </button>
                                    </li>
                                    <li class="nav-item">
                                        <button class="bottoni-icone">
                                            <a class="nav-link" href="#">
                                                <i class="fa-solid fa-user"></i>
                                            </a>
                                        </button>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </nav>
                </div>
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

header {
    width: 100%;
    background-color: $background;
    position: fixed;
    z-index: 10;

    .container {
        padding-right: 0em;

        .container-fluid {
            padding-right: 0em;
        }

        .logo {
            width: 80%;
            padding-right: 4em;
        }

        nav {
            padding: 1em;
            padding-right: 0em;
            color: $text-color;

            i {
                cursor: pointer;
            }

            .nav-item {
                padding: 0em 0.3em;

                .nav-link {
                    &.props {
                        text-transform: uppercase;
                        font-weight: 800;
                        font-size: 0.9rem;
                        padding: 0em 1.5em;

                        &.active {
                            color: $text-color-active;
                        }
                    }
                }
            }
        }
    }
}
</style>