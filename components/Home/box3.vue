<template>
    <div class="w-full mt-12">
        <swiper
    :slidesPerView="3"
    :spaceBetween="30"
    :loop="true"
    :pagination="{
      clickable: true,
    }"
    class="mySwiper"
    >
      <SwiperSlide class="bg-white rounded-md text-black" v-for="car in cars" :key="slide">
        <strong class="">
            <div class=" m-3 h-96 flex justify-center">
                <img class="h-full" :src="`/Home/box3/${car.img}`" alt="">
            </div>
            <div class="text-center">
                <div>{{car.name}}</div>
                <div>{{car.price}}</div>
            </div>    
        </strong>
      </SwiperSlide>
        </Swiper>
    </div>
</template>
<script>
export default{
    data(){
        return{
            cars:[
                {img:'img3.jpg',name:'BMW X1',price:'6,850,000'},
                {img:'img3.jpg',name:'BMW X1',price:'6,850,000'},
                {img:'img3.jpg',name:'BMW X1',price:'6,850,000'},
                {img:'img3.jpg',name:'BMW X1',price:'6,850,000'},
                {img:'img3.jpg',name:'BMW X1',price:'6,850,000'},
            ]
        }
    }
}
</script>
  