<template>
    <div class="container">
    	<NewQuote @quoteAdded='newQuote'></NewQuote>
    	<QuoteGrid :quotes='quotes'></QuoteGrid>
    </div>
</template>

<script>
	import QuoteGrid from './components/QuoteGrid.vue';
	import NewQuote from './components/NewQuote.vue';
    export default {
        data: function() {
        	return {
        		quotes: ['A famous quote'],
        		maxQuotes: 10
        	}
        },
        components: {
        	QuoteGrid,
        	NewQuote
        },
        methods: {
        	newQuote: function(quote) {
        		this.quotes.push(quote);
        	}
        }
    }
</script>

<style>
</style>
