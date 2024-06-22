<template>
    <div>
           <div class="h-screen flex justify-center pt-40 overflow-hidden relative" >
    <div class="w-full h-1/2" style="background: linear-gradient(
    to right,rgb(0 0 0 / 0.5),
    rgb(0 0 0/0)),
    url(/products/bmw-name.png);background-size: cover;">

    </div>
        <!-- <div class="absolute left-0 right-0 w-full" style="font-size: 500px;color: transparent;-webkit-text-stroke: 1px #ffff;">
            Nissan
        </div> -->
        <div class="absolute top-1/2 bottom-1/2 left-20" style="background: url();">
            <img class="" src="/products/shape.png" alt="">
            <div class="absolute left-1/2 text-5xl -top-1/2">
                Nissan Skyline GT-R
            </div>
        </div>
        <div class="absolute inset-0">
            <div class="h-4/5 flex items-end">
                <div class="w-1/2"></div>
                <div class="w-1/2">
                    <img class="w-full" src="/products/product-2.png" alt="">
                </div>
            </div>
            <div class="h-1/5 flex items-center ">
                <div class="w-1/3"></div>
            <div class="w-2/3 flex justify-between mx-12 text-2xl">
                <div>
                    <div>max speed</div>
                    <div>250 Km/h</div>
                </div>
                <div>
                    <div>Engin</div>
                    <div>4.4L</div>
                </div>
                <div>
                    <div>Power</div>
                    <div>600+ BHP</div>
                </div>
                <div>
                    <div>Mass</div>
                    <div>1960 Kg</div>
                </div>
            </div>
        </div>
        </div>


           </div> 
           <div class="h-screen bg-slate-500 flex justify-center items-center">
            <div class="relative">
                            <img class="h-full w-full" style="" src="/products/product-2-left.png" alt="">
                            <CarTextBox class="right-10 top-1/4 absolute" text="test saudhascakscas" name="box-1" />
                            <CarTextBox class="right-1/2 bottom-5 absolute" text="test saudhascakscas" name="box-2" />
                            <CarTextBox class="bottom-16 absolute" text="test saudhascakscas" name="box-3" />
                            <CarTextBox class="top-0 left-1/2 absolute" text="test saudhascakscas" name="box-4" />
            </div>
           </div>
    </div>

</template>
<script>
import $ from 'jquery'
export default{
    data(){
        return{
            cars:[
                {id:"1",img:'product-1.png',model:"Nissan",name:'Nissan Skyline GT-R',price:'6,850,000',max_speed:"250 Km/h",Engin:"4.4L",Power:"600+ BHP",Mass:"1960 Kg"},
                {id:"2",img:'product-3.png',model:"BMW",name:'BMW M8 2018',price:'6,850,000',max_speed:"250 Km/h",Engin:"4.4L",Power:"600+ BHP",Mass:"1960 Kg"},
            ],car:null
        }
    },mounted() {
        let cars = this.cars
        let ids = this.$route.params.id
        let cart = null
        console.log(this.$route.params.id)
        cars.map(car => {
            if(car.id == ids){
                cart = car
            }
        })
        this.car = cart
        $(".test").click(function(){
            $("#text-box").fadeToggle()
        })
    },
}
</script>
<style>
.text-box::after{
    content: '';
    width: 15px;
    height: 15px;
    position: absolute;
    left: 50%;
    bottom: -15px;
    clip-path: polygon(50% 100%, 0 0, 100% 0);
    background-color: rgb(226 232 240);
    transform: translate(-50%, -0%);
}
</style>