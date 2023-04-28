<script>
import "@fortawesome/fontawesome-free/css/all.css";
export default {
    name: "BuildTools",
}
</script>

<template>
    <section class="build-tools">
        <div class="container">
            <div class="row">
                <div class="col-7">
                    <h2>Build tools and extensive documention</h2>
                    <p>You can combine all the Landrick templateis into a single one,you can take a component from the
                        Applucation
                        theme and
                        use it in the Website.</p>
                    <ul>
                        <li><i class="fa-regular fa-circle-check"></i>
                            <p>Digital Marketing Solutions for Tomorrow</p>
                        </li>
                        <li><i class="fa-regular fa-circle-check"></i>
                            <p>Our Talented & Experienced Marketing Agency</p>
                        </li>
                        <li><i class="fa-regular fa-circle-check"></i>
                            <p>Create your own skin to match your brand</p>
                        </li>
                    </ul>
                    <button class="bottone-pieno">
                        <a href="#">Read More<i class="fa-solid fa-arrow-right"></i></a>
                    </button>
                </div>
                <div class="col-5">
                    <img src="../assets/img/1.png" alt="1">
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.row {
    padding: 4em 0em;

    h2 {
        width: 60%;
        padding-top: 2em;
    }

    p {
        padding: 1em 0em;
    }

    ul {
        margin: 0;
        padding: 0;
        padding-bottom: 1em;

        p {
            padding: 0em 0.5em;
            display: inline;
        }
    }

    .bottone-pieno {

        a,
        i {
            color: white;
            padding-left: 0.2em;
        }

        &:hover {

            a,
            i {
                color: $text-color-active;
            }
        }
    }
}
</style>