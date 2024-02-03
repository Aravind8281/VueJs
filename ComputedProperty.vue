<template>
    <div>
        <div v-for="item in cart" :key="item.id">
            {{ item.name }} - quantity : {{ item.quantity }}
        </div>
        <p>Total Price:{{ totalprice }} </p>
    </div>
</template>
<script>
    export default {
        name:"props-computed",
        data(){
            return{
                cart:[
                    {id:1,name:"Product A",price:10,quantity:2},
                    {id:2,name:"Product B",price:19,quantity:4}
                ]
            }
        },
        computed:{
            totalprice(){
                return this.cart.reduce((total,items)=>total+items.quantity*items.price,0)
            }
        }
    }

</script>
<style scoped>


</style>
