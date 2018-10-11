<template>
    <div class="container">
        <div class="row">
            <div>
               <app-quote class="cmp--Quote">
                   <h1 class="cmp--Quote-title" slot="title">{{ quoteTitle }}</h1>
                   <h4 class="cmp--Quote-content" slot="content">...not quite yet</h4>
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
@import url('https://fonts.googleapis.com/css?family=Titillium+Web:200,300,400,700');
    * {
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }
    html {
        font-size: 24px;
    }
    body {
        font-family: 'Titillium Web', serif;
        color: #f7f7f7;
        background-color: #006473;
        display: flex;
        flex: 1;
        justify-content: center
    }
    h1, h2, h3, h4, h5, h6 {
        font-weight: 200;
        margin: .5em 0;
    }

    .container {
        width: 70%;
    }
    .cmp--Quote {
        background-color: #03A9AC;
        margin: 1rem 0;
        padding: 1rem;

        width: 100%;
        text-align: center;

        box-shadow: 0px 0px 25px rgba(247, 247, 247, .0);
        transition: box-shadow 0.1s;

        border-radius: .75rem;
    }
    .cmp--Quote:hover {
        box-shadow: 0px 0px 25px rgba(247, 247, 247, .5);
    }

    .cmp--Quote-content {
        font-weight: 400;
    }

</style>
