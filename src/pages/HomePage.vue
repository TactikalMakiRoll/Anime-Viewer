<template>
    <page-header></page-header>
    <main class="featured">
        <div class="container">
            <h2 class="featured__title">カウボーイビバップ</h2>
            <h2 class="featured__translated-title">COWBOY BEBOP</h2>
            <div class="featured__top">
                <h3>Number in Top 10 Anime of all time</h3>
            </div>
            <p class="featured__description">Lorem ipsum dolor sit amet consectetur adipisicing elit. Numquam corporis esse molestiae veritatis adipisci nam totam dolores quod. Reiciendis, maxime? Quia sint harum corrupti dolore ea cum doloremque quod et?</p>
            <button class="featured__btn featured__btn--white">▶ Play</button>
            <button class="featured__btn">ⓘ More info</button>
        </div>
        <div >
            <img class="featured__background" src="../assets/images/testfeaturedBG.jpg" alt="showbg">
        </div>
    </main>
    <div class="container">
        <div class="sliders">
            <section class="slider">
                <a href="#">
                    <h2 class="slider__header">
                        Recommended
                        <div class="slider__header-explore">
                            <a href="#" class="slider__explore-link">Explore more</a>
                            >
                        </div>
                    </h2>
                </a>
                <Carousel class="slider__carousel" :touchDrag="false" :mouseDrag="false" :settings="state.settings" :breakpoints="state.breakpoints">
                    <Slide v-for="slide in 10" :key="slide">
                        <div class="slider__carousel-item">
                            
                        </div>
                    </Slide>

                    <template #addons>
                        <Navigation />
                    </template>
                </Carousel>
            </section>
        </div>
        
    </div>
</template>

<script setup>
    import {reactive} from 'vue';

    import PageHeader from "../components/PageHeader.vue";
    import { Carousel, Navigation, Slide } from 'vue3-carousel'
    import 'vue3-carousel/dist/carousel.css'
    
    const state = reactive({
        settings: {
            itemsToShow: 6,
            itemsToScroll:6,
        },
        breakpoints: {
            1920:{
                itemsToShow:6,
                itemsToScroll:6,
            }
        }
    })
</script>

<style lang="scss">
    .featured{
        margin-bottom: 7.25rem;
        padding-top: 9.5625rem;
        text-align: left;
    }

    .featured__title,.featured__translated-title,.featured__description, .slider__header{
        text-shadow:
            -1px -1px 0 #000,
            0   -1px 0 #000,
            1px -1px 0 #000,
            1px  0   0 #000,
            1px  1px 0 #000,
            0    1px 0 #000,
            -1px  1px 0 #000,
            -1px  0   0 #000;
    }

    .featured__title{
        font-size: 1.875em;
        margin-bottom: 1.875rem;
    }

    .featured__translated-title{
        font-size: 3.5em;
        font-weight: lighter;
        letter-spacing: 5px;
        margin-bottom: 1.875rem;
    }

    .featured__top{
        font-size: 1.875em;
        font-weight: bold;
        margin-bottom: 1rem;

    }

    .featured__description{
        margin: 1rem 0;
        font-size: 1.625em;
        font-weight: 300;
    }

    .featured__btn{
        font-size: 1.375em;
        background: rgba(0,0,0,0.25);
        padding: 0.875rem 1.625rem;
        border-radius: 4px;
        font-weight: bold;
    
    }

    .featured__btn:hover{
        cursor:pointer;
    }

    .featured__btn:active {
        transform: scale(0.98);
        box-shadow: 3px 2px 22px 1px rgba(0, 0, 0, 0.24);
    }

    .featured__btn--white{
        background-color: white;
        color:black;
    }

    .featured__btn+.featured__btn{
        margin-left: 1rem;
    }

    .featured__background{
        width: 100%;
        height: 50vw;
        max-height: 100vh;
        position: absolute;
        top:0;
        z-index: -1;
    }
    
    .sliders{
        margin-top: 2.8125rem;
    }
    
    .slider{
        margin-bottom: 1rem;
    }

    .slider__header{
        display: inline-block;
        font-size: 1.625em;
        margin-bottom: 0.75em;
        color:rgba(245,245,245,1);
    }
    
    .slider__header:hover{
        cursor: pointer;
        color: white;
    }

    .slider__header-explore{
        display: inline-block;
        visibility: hidden;
        transition: transform 1s ease;
        transform: translate(4rem);
        color:rgb(209, 233, 253);
    }

    .slider__explore-link{
        visibility: hidden;
        color:rgb(209, 233, 253);
        font-size: 0.01rem;
        transition: font 0.3s ease
    }

    @keyframes link-growth {
        0% {font-size: 0.01em;}
        100% {font-size:0.75em;}
    }

    .slider:hover > a .slider__header-explore{
        display: inline-block;
        visibility:visible;
        transform: translate(0);
    }

    .slider__header:hover .slider__explore-link{
        visibility: visible;
        font-size: 0.75em;
    }

    .carousel__icon{
        color:white;
        filter: invert(100%);
    }

    .carousel__prev--disabled, .carousel__next--disabled{
        display: none;
    }

    .carousel__next,.carousel__prev{
        transform: scale(2.5);
        color:white;
        filter: invert(100%);
    }

    .slider__carousel-item{
        width: 100%;
        min-height: 10rem;
        margin-right: 0.25rem;
        background: url(../assets/images/testSliderImg.jpg) no-repeat;
        background-size:cover;
        display: flex;
        justify-content: center;
        align-items: center;
    }
</style>