<template>
  <header class="header">
      <div class="header__logo">
          <img src="../assets/img/la-molisana-logo.png"/>
      </div>
      <nav class="header__nav">
          <ul>
              <li v-for="(link, index) in links" :key="index" :class="{active : link.current}"><a :href="link.url">{{link.text}}</a></li>
          </ul>
      </nav>
  </header>
</template>

<script>
export default {
    name: 'BaseHeader',
    data() {
        return {
            links: [
                {
                    text: "Home",
                    url: "#",
                    current: false,
                },
                {
                    text: "Prodotti",
                    url: "#",
                    current: true,
                },
                {
                    text: "Chi Siamo",
                    url: "#",
                    current: false,
                },
                {
                    text: "Contatti",
                    url: "#",
                    current: false,
                },
            ],
        }
    },
}
</script>

<style lang="scss" scoped>
@import '../assets/style/mixins.scss';

.header {
    text-align: center;

    &__logo { // header__logo
        margin-bottom: 1.25rem;
    }

    &__nav { // header__nav
        ul { // header__nav ul
            @include listInline;
            justify-content: center;
            a { // header__nav ul a
                display: inline-block;
                padding: 1.25rem;
                text-decoration: none;
                color: #000;
            }
            .active a { // header__nav ul .active a
                background-color: var(--secondary-color);
            }
        }
    }
}
</style>