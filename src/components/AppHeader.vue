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
                                    @click="elementoAttivo = index">
                                    <a class="nav-link props" href="#" :class="index === elementoAttivo ? 'active' : ''">{{
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
                        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                            aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                            <span class="navbar-toggler-icon"></span>
                        </button>
                        <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
                            <ul class="navbar-nav">
                                <li class="nav-item d-flex align-items-center gap-2">
                                    <input v-if="search === true" type="search" class="rounded w-100" placeholder="Search"
                                        aria-label="Search" aria-describedby="search-addon" />
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
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.container {
    width: 80%;

    .logo {
        width: 80%;
        padding-right: 4em;
    }

    nav {
        padding: 1em;
        color: $text-color;

        i {
            cursor: pointer;
        }

        .nav-item {
            padding: 0em 0.3em;

            .nav-link {
                &.props {
                    text-transform: uppercase;
                    font-weight: 600;
                    font-size: 0.8rem;
                    padding: 0em 1.5em;

                    &.active {
                        color: $text-color-active;
                    }
                }
            }

            .bottoni-icone {
                background-color: $background-button;
                border-style: none;
                display: flex;
                justify-content: center;
                align-items: center;
                width: 2rem;
                height: 2rem;
                font-size: 1rem;
                border-radius: 5px;
                box-shadow: 3px 5px 5px rgb(116, 116, 116);

                i {
                    color: $text-color-active;
                }

                &:hover {
                    background-color: $text-color-active;

                    i {
                        color: $background-button;
                    }
                }

            }
        }
    }
}
</style>