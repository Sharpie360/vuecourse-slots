<template>
    <div class="container">
        <div class="row">
            <div>
               <app-quote class="cmp--Quote">
                   <h1>{{ quoteTitle }}</h1>
                   <h4>...not quite yet</h4>
               </app-quote>
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue'
    export default {
        data () {
            return {
                quoteTitle: 'An Awesome Quote'
            }
        },
        components: {
            'app-quote': Quote
        }
    }
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=Kodchasan:200,300,400,700');
    html {
        font-size: 24px;
    }
    body {
        font-family: 'Kodchasen', serif;
        color: #f7f7f7;
        background-color: #006473;
    }

    .cmp--Quote {
        background-color: #03A9AC;
        border: 2px solid #212121;

        padding: 1rem;
        width: 1140px;
        text-align: center;
        margin: 1rem auto;
    }

</style>
