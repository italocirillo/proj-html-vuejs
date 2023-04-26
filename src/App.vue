<script>
import AppHeader from './components/AppHeader.vue';

export default {
  components: { AppHeader },
  data() {
    return {
      elementiHeader: ["Home", "Landing", "Pages", "Docs"],
    }
  }
}
</script>

<template>
  <AppHeader :arrayHeader="elementiHeader" />
</template>

<style lang="scss">
@use "./styles/general.scss";
</style>

