<template>
    <div class="row cart-item-row">
        <div class="col-md-6">
            <Product :product="product" />
        </div>
        <div class="col-md-4">
            <div class="row">
                <div class="col-md-5">
                    <button class="btn btn-primary btn-block">+</button>
                </div>
                <div class="col-md-2 text-center">{{product.quantity}}</div>
                <div class="col-md-5">
                    <button class="btn btn-warning btn-block">-</button>
                </div>
            </div>
            <div class="row cart-remove-button">
                <div class="col-md-12">
                    <button class="btn btn-danger btn-block">Remove Item</button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Product from "./Product.vue"
export default {
    name : "CartItem",
    props : ['product'],
    components : {
        Product
    }
}
</script>
<style scoped>
.cart-item-row{
    border-bottom: 1px solid #ccc;
    margin-top: 20px;
}
.cart-remove-button{
    margin-top: 10px;
}
</style>