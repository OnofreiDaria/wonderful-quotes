<template>
  <div id="app">
    <div class="container">
      <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>

  </div>
</template>

<script>
  import QuoteGrid from "./components/QuoteGrid";

  export default {

  name: 'App',
  data() {
    return {
      quotes: [
        'Just a quote to see smth'
      ],
      maxQuotes: 10
    }
  },
  components: {
    appQuoteGrid: QuoteGrid
  }
}
</script>

<style>
</style>
