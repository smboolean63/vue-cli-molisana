<template>
  <section>
      <h2>Offerte Speciali</h2>
      <div class="offers__list">
        <CardProduct title="Spaghetti in offerta" image="https://www.lamolisana.it/wp-content/uploads/2021/04/1-spaghetto-quadrato.jpg"/>
        <CardProduct title="Mezze maniche in offerta"/>
      </div>
  </section>
</template>

<script>
import CardProduct from '../commons/CardProduct.vue';

export default {
    name: 'SectionOffers',
    components: {
        CardProduct,
    }
}
</script>

<style lang="scss" scoped>
.offers {
    &__list {
        display: flex;

        > * {
            width: 50%;
        }
    }
}
</style>