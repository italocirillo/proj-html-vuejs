<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  components: { AppHeader, AppMain, AppFooter },
  data() {
    return {
      elementiHeader: ["Home", "Landing", "Pages", "Docs"],
      affiliati: [
        {
          url: "amazon.svg",
          name: "amazon",
        },
        {
          url: "google.svg",
          name: "google",
        },
        {
          url: "lenovo.svg",
          name: "lenovo",
        },
        {
          url: "paypal.svg",
          name: "paypal",
        },
        {
          url: "shopify.svg",
          name: "shopify",
        },
        {
          url: "spotify.svg",
          name: "spotify",
        },
      ],
      company: ["About us", "Services", "Team", "Pricing", "Project", "Careers", "Blog", "Login"],
      usefullLinks: ["Terms of Services", "Privacy Policy", "Documentation", "Changelog", "Component"],
      carteDiCredito: [
        {
          url: "american-ex.png",
          name: "american-ex",
        },
        {
          url: "discover.png",
          name: "discover",
        },
        {
          url: "master-card.png",
          name: "master-card",
        },
        {
          url: "paypal.png",
          name: "paypal",
        },
        {
          url: "visa.png",
          name: "visa",
        },
      ],
    }
  }
}
</script>

<template>
  <AppHeader :arrayHeader="elementiHeader" />
  <AppMain :affiliati="affiliati" />
  <AppFooter :company="company" :usefullLinks="usefullLinks" :carteDiCredito="carteDiCredito" />
</template>

<style lang="scss">
@use "./styles/general.scss";
@use "./styles/partials/variables" as*;

.container {
  width: 80%;
}

p {
  color: $text-color-light;
  font-size: 1rem;
  font-weight: 500;
}

i {
  color: $text-color-active;
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

  &:hover {
    background-color: $text-color-active;

    i {
      color: $background-button;
    }
  }

}

.bottone-pieno {
  background-color: $text-color-active;
  color: white;
  padding: 0.5em 1em;
  border-radius: 5px;
  box-shadow: 4px 4px 10px black;
  font-weight: 700;

  &:hover {
    background-color: white;
    color: $text-color-active;
    border: 2px solid $text-color-active;
    padding: 0.4em 0.9em;
  }
}

.bottone-vuoto {
  background-color: white;
  border: 2px solid $text-color-active;
  color: $text-color-active;
  padding: 0.4em 0.9em;
  border-radius: 5px;
  box-shadow: 4px 4px 10px black;
  font-weight: 700;

  &:hover {
    background-color: $text-color-active;
    color: white;
  }
}
</style>

