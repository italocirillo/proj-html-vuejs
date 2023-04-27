<script>
export default {
    name: "AppFooter",
}
</script>

<template>
    <footer>
        <div class="container">
            <ul class="row align-items-start">
                <li class="col">
                    One of three columns
                </li>
                <li class="col">
                    One of three columns
                </li>
                <li class="col">
                    One of three columns
                </li>
                <li class="col">
                    One of three columns
                </li>
            </ul>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

footer {
    background-color: #202942;
    color: white;
    padding: 0em;

    ul {
        padding: 0em;
        margin: 0em;
        gap: 1em;

        .col {
            padding: 0em;
        }
    }
}
</style>