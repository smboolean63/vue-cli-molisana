<template>
  <header class="header">
      <div class="header__logo">
          <!-- <img src="../assets/img/la-molisana-logo.png"/> -->
          <img :src="require(`../../assets/img/${logoSrc}`)" alt="">
      </div>
      <nav class="header__nav">
          <ul>
              <li v-for="(link, index) in links" :key="index"><a @click.prevent="onClickMenuItem(link)" :href="link.url" :class="{active : link.current}">{{link.text}}</a></li>
          </ul>
      </nav>
  </header>
</template>

<script>
export default {
    name: 'BaseHeader',
    data() {
        return {
            logoSrc: 'la-molisana-logo.png',
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
    methods: {
        onClickMenuItem(item) {
            item.current = !item.current;
        }
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/mixins.scss';

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
                &.active, &:hover { // header__nav ul a.active
                    background-color: var(--secondary-color);
                }
            }
        }
    }
}
</style>