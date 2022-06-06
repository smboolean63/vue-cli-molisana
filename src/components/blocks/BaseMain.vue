<template>
  <main>
      <div class="container">
        <SectionProducts/>
        <SectionOffers/>
      </div>
  </main>
</template>

<script>
import SectionProducts from '../sections/SectionProducts.vue';
import SectionOffers from '../sections/SectionOffers.vue';

export default {
    name: 'BaseMain',
    components: {
      SectionProducts,
      SectionOffers,
    }
}
</script>

<style lang="scss">
main {
  background-image: url('../../assets/img/fondo-pag-speciali.jpg');
  padding: 2.5rem 0;
  margin: 2.5rem 0;

  h2, h3 {
    text-align: center;
  }
}
</style>