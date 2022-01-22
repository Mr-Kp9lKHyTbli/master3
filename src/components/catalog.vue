<template>
    <div class="catalog">
        <label id="bestsellers">
            BESTSELLERS: <br>
            34
        </label>
        <shop-items 
            v-for="product in products"
            :key="product.article"
            v-bind:product_data="product"
            @sendArticle="showArticle"
        />
    </div>
</template>

    <script>
    import ShopItems from './shop-items.vue'

    export default {
        name: "catalog",
        components: {
            ShopItems,
        },
        props: {},
        data() {
            return {
                products: [
                    {
                        image: "1.jpg",
                        name: "Converse Kids 70",
                        price: 49.99,
                        article: "B1",
                        available: true
                    },
                    {
                        image: "2.jpg",
                        name: "Converse Chuck 70",
                        price: 49.99,
                        article: "B2",
                        available: true
                    },
                    {
                        image: "3.jpg",
                        name: "Converse Chuck 70 Renew High Top",
                        price: 50.99,
                        article: "B3",
                        available: true
                    },
                    {
                        image: "4.jpg",
                        name: "Converse Pro Chuck 70",
                        price: 64.99,
                        article: "B4",
                        available: true
                    },
                    {
                        image: "5.jpg",
                        name: "Converse Winter Chuck 70",
                        price: 79.99,
                        article: "B5",
                        available: true
                    },
                    {
                        image: "6.jpg",
                        name: "Conver Winter Chuck 70 Full Black",
                        price: 129.99,
                        article: "B6",
                        available: true
                    },
                    {
                        image: "7.jpg",
                        name: "Converse Winter Chuck 70 Black/White",
                        price: 99.99,
                        article: "B7",
                        available: true
                    }
                ]
            }
        },
        computed: {},
        methods: {
            showArticle(data){
                console.log(data)
            }
        }
    }
    </script>

<style>

.catalog {
    position: absolute;
max-width: 1400px;
height: 1507px;
left: 100px;
top: 403px;
display: flex;
flex-wrap: wrap;
margin: 0 auto;

}

#bestsellers {
    position: absolute;
    left: 0px;
top: 0px;
font-family: Inter;
font-style: normal;
font-size: 40px;
}

</style>