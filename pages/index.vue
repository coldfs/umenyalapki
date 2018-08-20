<template>
  <section class="container">
    <div>
      <h1 class="title">Lapki - Randomizer</h1>
      <h2 class="subtitle">я ничего не хочу решать, у меня лапки</h2>
      <rando/>
    </div>
  </section>
</template>

<script>
import Rando from '~/components/Rando.vue'

export default {
  components: {
    Rando
  }
}
</script>

<style>

.container {
  min-height: 100vh;
  /* display: flex; */  
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 50px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 21px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

</style>

