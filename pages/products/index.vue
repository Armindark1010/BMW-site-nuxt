<template>
    <div class="flex justify-around">
        <div class="w-1/3 h-96" v-for="car in cars">
            <nuxt-link :to="`/products/product-${car.id}`">
            <div>
                <img class="w-full h-full" :src="`/products/${car.img}`" alt="">
            </div>
            <div class="text-center text-4xl text-black bg-white">
                {{ car.name }}
            </div>
            </nuxt-link>
        </div>
    </div>
</template>
<script>
export default{
    data(){
        return{
            cars:[
                {id:"1",img:'product-1.png',model:"Nissan",name:'Nissan Skyline GT-R',price:'6,850,000',max_speed:"250 Km/h",Engin:"4.4L",Power:"600+ BHP",Mass:"1960 Kg"},
                {id:"2",img:'product-3.png',model:"BMW",name:'BMW M8 2018',price:'6,850,000',max_speed:"250 Km/h",Engin:"4.4L",Power:"600+ BHP",Mass:"1960 Kg"},
            ]
        }
    }
}
</script>