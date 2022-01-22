<template>
    <div id="back">
        <label id="s-shop">
            S-SHOP
        </label>

        <label id="cat">
            Catalog
        </label>

        <label id="prof">
            Profile
        </label>

        <button class="basket_btn btn" onclick="basket_window.style.display='flex';">
            Basket({{p}})
        </button>

        <div id="border"></div>

        <label id="search">
            Search
        </label>

        <label id="categ">
            Product category
        </label>

        <label id="sale">
            Sale
        </label>

        <button class="apply btn">Apply</button>

        <select class="sel_search">
            <option>Converse</option>
            <option>Converse 2</option>
        </select>

        <select class="sel_cat">
            <option>Sneakers</option>
            <option>Boots</option>
        </select>

        <select class="sel_sale">
            <option>Bestsellers</option>
            <option>Max. sale</option>
        </select>
        
        <catalog />
        <div class="down">
            <label id="s-shop2">
                S-SHOP
            </label>
            <label id="copy">
                Copyright
            </label>
            <label id="contacts">
                Contacts
            </label>
        </div>






        <div class="basket_window">
            <label class="prof_b">
            Profile
            </label>

            <button class="basket_btn_b btn">
            Basket({{p}})
            </button>


            <div class="border_b"></div>


            <label class="total">
                TOTAL
            </label>



            <label class="subtotal">
                Subtotal:
            </label>

            <label class="subtotal_cost">
                {{cost}}
            </label>



            <label class="sale_b">
                Sale:
            </label>

            <label class="sale_cost">
                {{sales}}
            </label>



            <label class="content_b">
                Content:
            </label>

            <button class="remove_b">
                Remove all
            </button>


            <div class="border_b_2"></div>

            <label class="order">Order Total:</label>

            <label class="total_sum"> {{order_sum}} </label>

            <div class="border_b_3"></div>


            <button class="checkout_btn btn" onclick="this.parentElement.style.display='none';">Checkout ></button>

        </div>


    </div>
    
    
</template>

<script>

import Catalog from './catalog.vue'

export default {
    name: 'shop',
  components: {
    Catalog,
  }

}
</script>

<style>

#back{
    display: flex;
    position: relative;
    width: 1600px;
    height: 2140px;

    background: #FFFFFF;
}

#s-shop{
    position: absolute;
    left: 100px;
    top: 35px;
    font-family: Inter;
    font-style: normal;
    font-size: 24px;
}

#cat{
    position: absolute;
    left: 455px;
    top: 39px;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #FF6B00;
}

#prof{
    position: absolute;
    left: 1320px;
    top: 39px;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #000000;
}

.basket_btn{
    border: none;
    background-color: inherit;
    cursor: pointer;
    position: absolute;
    left: 1419px;
    top: 39px;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #000000;
}

#border{
    position: absolute;
    left: 100px;
    top: 100px;
    width: 1400px;
    border: 1px solid #BDBDBD;
}

#search{
    position: absolute;
    top: 180px;
    left: 100px;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #000000;
}

#categ{
    position: absolute;
    top: 180px;
    left: 455px;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #000000;
}

#sale{
    position: absolute;
    top: 180px;
    left: 810px;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #000000;
}

.sel_search{
    position: absolute;
    top: 222px;
    left: 100px;
    width: 335px;
    height: 61px;
    background: #F5F5F5;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #000000;
}

.sel_cat{
    position: absolute;
    top: 222px;
    left: 455px;
    width: 335px;
    height: 61px;
    background: #F5F5F5;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #000000;
}

.sel_sale{
    position: absolute;
    top: 222px;
    left: 810px;
    width: 335px;
    height: 61px;
    background: #F5F5F5;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #000000;
}

.apply{
    position: absolute;
    top: 222px;
    left: 1165px;
    width: 336px;
    height: 61px;
    background: #1B1B1B;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #FFFFFF;
    cursor: pointer;
}

#s-shop2{
    position: absolute;
    top: 40px;
    left: 100px;
    color: white;
    font-size: 24px;
    font-family: Inter;
}

#copy{
    position: absolute;
    top: 43px;
    left: 1295px;
    color: white;
    font-size: 18px;
    font-family: Inter;
}

#contacts{
    position: absolute;
    top: 43px;
    left: 1421px;
    color: white;
    font-size: 18px;
    font-family: Inter;
}

.down{
    position: absolute;
    top: 2030px;
    width: 1600px;
    height: 110px;
    background: black;
}





.basket_window{
    position: absolute;
    width: 455px;
    height: 784px;
    left: 1145px;
    top: 0px;
    background: #FFFFFF;
    display: block;
}


.prof_b{
    position: absolute;
    left: 175px;
    top: 39px;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #000000;
}

.basket_btn_b{
    border: none;
    background-color: inherit;
    cursor: pointer;
    position: absolute;
    left: 273px;
    top: 39px;
    font-family: Inter;
    font-style: normal;
    font-size: 18px;
    color: #FF6B00;
}

.border_b{
    position: absolute;
    left: 0px;
    top: 100px;
    width: 455px;
    border: 1px solid #BDBDBD;
}

.total{
    position: absolute;
    top: 120px;
    left: 41px;
    color: #000000;
    font-size: 24px;
    font-family: Inter;
}

.subtotal{
    position: absolute;
    left: 41px;
    top: 179px;
    font-family: Inter;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    color: #000000;
}

.subtotal_cost{
    position: absolute;
    left: 300px;
    top: 179px;
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 19px;
    text-align: right;
    color: #000000;
}



.sale_b{
    position: absolute;
    left: 41px;
    top: 218px;
    font-family: Inter;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    color: #000000;
}

.sale_cost{
    position: absolute;
    left: 300px;
    top: 218px;
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 19px;
    text-align: right;
    color: #000000;
}



.content_b{
    position: absolute;
    left: 41px;
    top: 257px;
    font-family: Inter;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    color: #000000;
}

.remove_b{
    position: absolute;
    left: 272px;
    top: 257px;
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 19px;
    text-align: right;
    text-decoration-line: underline;
    color: #000000;
    border: none;
    background-color: inherit;
    cursor: pointer;
}



.border_b_2{
    position: absolute;
    left: 0px;
    top: 316px;
    width: 455px;
    border: 1px solid #BDBDBD;
}

.order{
    position: absolute;
    left: 41px;
    top: 336px;
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 20px;
    color: #000000;
}

.total_sum{
    position: absolute;
    left: 276px;
    top: 336px;
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 20px;
    text-align: right;
    color: #000000;
}

.border_b_3{
    position: absolute;
    left: 0px;
    top: 380px;
    width: 455px;
    border: 1px solid #BDBDBD;
}




.checkout_btn{
    position:absolute;
    bottom: 0px;
    width: 455px;
    height: 84px;
    left: 0;
    background: #000000;
    cursor: pointer;
    text-align: left;
    font-family: Inter;
    font-style: normal;
    font-weight: 500;
    font-size: 20px;
    line-height: 24px;
    color: #FFFFFF;
}

</style>