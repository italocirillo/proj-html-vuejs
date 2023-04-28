<script>
import "@fortawesome/fontawesome-free/css/all.css";
import Titolo from "./Titolo.vue";
export default {
    name: "Quickstart",
    components: { Titolo }
}
</script>

<template>
    <div class="quick-start">

        <div class="container">
            <h2>Quickstart</h2>
            <Titolo class="p-0" :titolo="`Awesome isn't it? Let's dive in`" />
            <div class="lista">
                <ul>
                    <li class="active">npm</li>
                    <li>nuget</li>
                    <li>spm</li>
                    <li>github</li>
                </ul>
            </div>

        </div>
    </div>
</template>


<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.quick-start {
    text-align: center;
    padding-top: 5em;

    h2 {
        color: $text-color-active;
        font-size: 1rem;
        padding-bottom: 1em;
    }

    .lista {
        background-color: #3b4858;
        width: 50%;
        margin: 0 auto;
        border-radius: 10px;

        ul {
            background-color: #4f5a69;
            display: flex;
            padding: 0.4em;
            align-items: center;
            justify-content: space-between;
            border-radius: 5px;

            li {
                width: calc(100%/4);
                padding: 1em;
                color: white;
                background-color: #4f5a69;
                cursor: pointer;

                &.active {
                    background-color: #3b4858;
                    border-radius: 10px;
                    border: 2px solid #4f5a69;
                    border-right: none;
                }
            }
        }
    }


}
</style>