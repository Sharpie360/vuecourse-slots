<template>
    <div class="container">
        <div class="row">
            <div>
                <div id="view-btns">
                    <button @click="selectedComponent = 'app-quote'">Quote</button>
                    <button @click="selectedComponent = 'app-author'">Author</button>
                    <button @click="selectedComponent = 'app-new'">New Quote</button>
                </div>
                {{ selectedComponent }}
                <component :is="selectedComponent">
                    <h1 slot="title">{{ quoteTitle }}</h1>
                    <h3 class="content" slot="content">...not quite yet</h3>

                </component>
               <!-- <app-quote class="cmp--Quote">
                   <h1 class="cmp--Quote-title" slot="title">{{ quoteTitle }}</h1>
                   <h4 class="cmp--Quote-content" slot="content">...not quite yet</h4>
               </app-quote> -->
            </div>
        </div>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue'
    import Author from './components/Author.vue'
    import New from './components/New.vue'
    export default {
        data () {
            return {
                quoteTitle: 'An Awesome Quote',
                selectedComponent: 'app-quote'
            }
        },
        components: {
            'app-quote': Quote,
            'app-author': Author,
            'app-new': New
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
        justify-content: center;
        text-align: center;
    }
    h1, h2, h3, h4, h5, h6 {
        font-weight: 200;
        margin: .5em 0;
    }

    .container {
        width: 70%;
    }
    

</style>
