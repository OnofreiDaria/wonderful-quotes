<template>
  <div id="app">
    <div class="container">
      <app-new-quote @quoteAdded="newQuote"></app-new-quote>
      <app-quote-grid :quotes="quotes"></app-quote-grid>
    </div>

  </div>
</template>

<script>
  import QuoteGrid from "./components/QuoteGrid";
  import NewQuote from "./components/NewQuote";
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
  methods: {
    newQuote(quote) {
      this.quotes.push(quote);
    }
  },

  components: {
    appQuoteGrid: QuoteGrid,
    appNewQuote: NewQuote
  }
}
</script>

<style>
</style>
