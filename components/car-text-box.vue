<template>
    <div>
        <div v-click-outside="outside"  class=" cursor-pointer w-10 h-10 rounded-full" style="background-color:#ffffff98;">
                                <div :class="`c-${name}`" class="h-6 w-6 absolute flex justify-center items-center bg-slate-100 top-1/2 left-1/2 rounded-full" style="  transform: translate(-50%, -50%);">
                                <span :class="name" class="text-black">
                                    X
                                </span>
                                </div>
                                <div :class="name"  class="md:w-48 w-24 text-box bg-slate-200 text-black rounded-md p-3 absolute z-50 left-1/2" style="top: 0;  transform: translate(-50%,calc(-100% - 20px));">{{ text }}</div>
        </div>
    </div>
</template>
<script>
import $ from 'jquery'

export default {
    data(){
        return{
            tf:false
        }
    },
    props: ['text', 'name'],
    methods: {
        outside(){
            if(this.tf){
                $(`.${this.name}`).fadeOut();
                this.tf = !this.tf
            }
            console.log("1")
        }
    },
    mounted() {
        $(`.${this.name}`).fadeOut();
        console.log(this.tf)
        $(`.c-${this.name}`).click(() => {
            this.tf = !this.tf
            if(this.tf){
                $(`.${this.name}`).fadeIn();
            }else{
                $(`.${this.name}`).fadeOut();
            }
        });
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