<script>
export default {
    name: "Titolo",
    props: {
        titolo: String,
    }
}
</script>

<template>
    <div class="titolo">
        <h2>{{ titolo }}</h2>
        <p>Start working with <span>Landrick</span> that can provide everything you need to
            generate
            awareness,drive
            traffic, connect
        </p>
    </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/variables" as*;

.titolo {
    text-align: center;
    width: 60%;
    margin: 0 auto;
    padding-top: 8em;
    padding-bottom: 1em;

    h2 {
        font-weight: 600;
    }

    p {
        font-weight: 700;
        padding: 1em 0em;

        span {
            color: $text-color-active;
        }
    }
}
</style>