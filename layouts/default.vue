<template>
    <div>
        <nav class="fixed top-0 left-0 right-0" style="z-index: 999;">
            <div class="flex">
            <div class="text-4xl h-16 flex w-1/3 items-end relative">
                <img class="h-20 w-20 absolute -bottom-8 left-16" src="/favicon.png" alt="">
            </div>
            <div class="flex items-start w-2/3 justify-between mx-12 text-2xl">
            <nuxt-link to="/">
                <div>
                    <div>
                        Home
                    </div>
                    <div id="" class="active">
                    </div>
                </div>
            </nuxt-link>
            <nuxt-link to="/products">
                <div>
                    <div>
                        products
                    </div>
                    <div id="" class="active">
                    </div>
                </div>
            </nuxt-link>
                <div>Pricing</div>
                <div>Services</div>
                <div>Contact</div>
            </div>
            </div>
            <div>
                <img class="w-full" src="/imgs/Line-nav.png" alt="">
            </div>
        </nav>
        <slot />
    </div>
</template>
<style>
.router-link-active .active{
background-color: white;
height: 2px;
margin-top: 3px;
animation: active 2s infinite;

}
@keyframes active{
    0%{opacity: 1;}
    50%{opacity: 0;}
    100%{opacity: 1;}
}
</style>