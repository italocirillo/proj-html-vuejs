<script>
export default {
    name: "AppFooter",
    props: {
        company: Array,
        usefullLinks: Array,
        carteDiCredito: Array
    },
    methods: {
        getImagePath(image) {
            return new URL(`../assets/img/${image}`, import.meta.url).href;
        }
    }
}
</script>

<template>
    <footer>
        <div class="container">
            <ul class="row align-items-start">
                <!-- Landrick -->
                <li class="col-4">
                    <ul>
                        <img class="logo" src="../assets/img/logo-light.png" alt="logo-footer">
                        <p>Start working width Landrick that can provide everything you need to generate awareness,drive
                            traffic,connect.
                        </p>
                        <ul class="icone">
                            <li><a href="#" class="bottoni-icone"><i class="fa-brands fa-facebook-f"></i></a></li>
                            <li><a href="#" class="bottoni-icone"><i class="fa-brands fa-instagram"></i></a></li>
                            <li><a href="#" class="bottoni-icone"><i class="fa-brands fa-twitter"></i></a></li>
                            <li><a href="#" class="bottoni-icone"><i class="fa-brands fa-linkedin-in"></i></a></li>
                        </ul>
                    </ul>
                </li>
                <!-- Company -->
                <li class="col-2">
                    <h3>Company</h3>
                    <ul>
                        <li class="items" v-for="(elemento, index) in company" :key="index">
                            <i class="fa-solid fa-chevron-right"></i>
                            <p>{{ elemento }}</p>
                        </li>
                    </ul>
                </li>
                <!-- Usefull Links -->
                <li class="col-2">
                    <h3>Usefull Links</h3>
                    <ul>
                        <li class="items" v-for="(elemento, index) in usefullLinks" :key="index">
                            <i class="fa-solid fa-chevron-right"></i>
                            <p>{{ elemento }}</p>
                        </li>
                    </ul>
                </li>
                <!-- Newsletter -->
                <li class="col-4 newsletter">
                    <h3>Newsletter</h3>
                    <p>Sign up and receive the latest tips via email.</p>
                    <strong>
                        <p>Write your email <span>*</span></p>
                    </strong>
                    <div class="input-group mb-3">
                        <span class="input-group-text" id="basic-addon1"><i class="fa-regular fa-envelope"></i></span>
                        <input type="email" class="form-control" placeholder="Your email :" aria-label="Email"
                            aria-describedby="basic-addon1">
                    </div>
                    <button class="bottone-pieno"><a href="#">Subscribe</a></button>
                </li>
            </ul>
        </div>
        <hr>
        <div class="footer-bottom">
            <div class="container">
                <div class="informazioni">
                    <p>&#169; 2023 Landrick. Designed by Shreethemes. Created with <span>&hearts;</span> by @italo.cirillo.
                    </p>
                    <ul class="carte-credito">
                        <li v-for="(elemento, index) in carteDiCredito" :key="index">
                            <img :src="getImagePath(elemento.url)" :alt="elemento.name">
                        </li>
                    </ul>
                </div>
            </div>
            <a href="#"><button class="bottoni-icone"><i class="fa-solid fa-arrow-up"></i></button></a>
        </div>

    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

footer {
    background-color: #202942;
    color: white;
    padding-top: 4em;

    ul {
        padding: 0em;
        margin: 0em;
        flex-wrap: nowrap;

        .col-4 {
            padding-right: 4em;
        }

        li {
            padding: 0em;

            h3 {
                font-weight: 600;
                font-size: 1.5rem;
                padding-bottom: 0.8em;
            }
        }

        img {
            width: 40%;
        }

        p {
            padding: 2em 0em;
            font-weight: 700;
        }

        .icone {
            display: flex;
            gap: 0.5em;

            .bottoni-icone {
                background-color: inherit;
                border: 1px solid $text-color-light;
                box-shadow: none;

                i {
                    color: $text-color-light;
                }

                &:hover {
                    background-color: $text-color-light;

                    i {
                        color: #202942;
                    }
                }
            }
        }

        .items {
            padding-bottom: 1em;

            i {
                color: $text-color-light;
            }

            p {
                display: inline;
                padding-left: 0.5em;
                font-size: 1.2rem;
                font-weight: 500;
            }
        }

        .newsletter {
            padding-left: 4em;
            padding-right: 0em;

            p {
                padding: 0em;
            }

            strong {
                p {
                    font-weight: 900;
                    font-size: 0.8rem;
                }

                span {
                    color: red;
                }
            }

            .input-group {

                span {
                    background-color: #27314f;
                    border: none;
                    border-radius: 10px;

                    i {
                        padding: 0.5em 1em;
                        color: $text-color-light;
                    }
                }

                input {
                    background-color: #27314f;
                    color: white;
                    border: none;
                    border-radius: 10px;

                    &::placeholder {
                        color: $text-color-light;
                    }

                    &.form-control {
                        box-shadow: none;
                    }
                }

            }

            .bottone-pieno {
                margin-top: 1em;
                width: 100%;
                background-color: #212e51;
                border-radius: 10px;
                box-shadow: 1px 1px 10px 1px #2e51c6;
                padding: 1em 0em;

                a {
                    color: #2e51c6;
                }

                &:hover {
                    background-color: rgb(176, 210, 242);
                }
            }
        }

    }

    hr {
        color: #485c93;
        margin: 0em;
        margin-top: 4em;
    }

    .footer-bottom {
        position: relative;

        .container {

            .informazioni {
                padding: 1.5em 0em;
                display: flex;
                align-items: center;
                justify-content: space-between;

                p {
                    font-size: 0.8rem;
                    margin-bottom: 0;
                }

                span {
                    color: red;
                }

                .carte-credito {
                    text-align: end;
                    display: flex;

                    li {
                        padding-left: 0em;
                    }

                    img {
                        width: 85%;
                    }

                }
            }
        }

        .bottoni-icone {
            position: absolute;
            top: 50%;
            right: 0;
            margin-right: 1em;
            transform: translateY(-50%);
            background-color: $text-color-active;
            box-shadow: 2px 2px 10px rgb(0, 96, 128);

            i {
                color: white;
            }

            &:hover {
                background-color: white;

                i {
                    color: $text-color-active;
                }
            }
        }
    }

}
</style>