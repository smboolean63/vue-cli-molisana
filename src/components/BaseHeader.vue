<template>
  <header class="header">
      <div class="header__logo">
          <img src="../assets/img/la-molisana-logo.png"/>
      </div>
      <nav class="header__nav">
          <ul>
              <li><a href="#">Link</a></li>
              <li><a href="#">Link</a></li>
              <li><a href="#">Link</a></li>
              <li class="active"><a href="#">Link</a></li>
              <li><a href="#">Link</a></li>
          </ul>
      </nav>
  </header>
</template>

<script>
export default {
    name: 'BaseHeader',
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