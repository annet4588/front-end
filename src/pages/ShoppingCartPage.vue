
<template>
    <h1>Shopping Cart</h1>
    <div v-if="cartItems.length > 0">
        <ShoppingCartList :products="cartItems"/>
        <button class="checkout-button">Proceed to Checkout</button>
    </div>
    <div v-if="cartItems.length === 0">You have no items in your cart</div> 
</template>  

<script>
import ShoppingCartList from '@/components/ShoppingCartList.vue'
import {cartItems} from '../temp-data'

export default{
    name: "ShoppingCartPage",
    components: {
        ShoppingCartList,
    },
    data(){
        // eslint-disable-next-line no-unused-vars
        const unusedVariable = cartItems; // This line will not trigger the 'no-unused-vars' warning
        return{
            cartItems,
        }
    }
}
</script>