<template>
  <div class="row">
    <app-quote v-for="(quote, index) in quotes" :key="quote.index" @click.native="deleteQuote(index)"> {{ quote }}</app-quote>
  </div>
</template>

<script>
  import Quote from "./Quote";
  export default {
    props: ['quotes'],
    methods: {
      deleteQuote(index) {
        this.$emit('quoteDeleted', index);
      }
    },
    components: {
      appQuote: Quote
    }
  }
</script>

<style>

</style>
