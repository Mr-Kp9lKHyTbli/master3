<template>
    <div class="shopitems">
        <img :src=" require('../assets/images/' + product_data.image) " alt="img">
        <p class="shop-items_name">{{product_data.name}}</p>
        <p class="shop-items_price">${{product_data.price}}</p>
        <button class="shop-items_add_btn btn"  @click="sendDataToParent">Add to basket</button>
    </div>
</template>

<script>
export default {
    name: "shop-items",
    props: {
        product_data: {
            type: Object,
            default () {
                return {}
            }
        }
    },
    data() {
        return {}
    },
    computed: {},
    methods: {
        sendDataToParent(){
           // this.$emit(var event: 'sendArticle', this.product_data.article)
        }
    }
}
</script>

<style>

.shopitems {

    margin: 5px;
    
}

.shop-items_name{
    font-family: Inter;
    font-style: normal;
    font-size: 16px;
    color: #000000;
    text-align: left;
}

.shop-items_price{
    font-family: Inter;
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    color: #000000;
    text-align: left;
}

.shop-items_add_btn{
    width: 335px;
    height: 60px;
    background: #2E2E2E;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #FFFFFF;
    text-align: left;
    outline: none;
    cursor: pointer;
}



</style>