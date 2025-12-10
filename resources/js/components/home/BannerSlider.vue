<template>
    <div class="product-slider">
        <swiper
            :slides-per-view="slidesPerView"
            :space-between="20"
            :pagination="{ clickable: true }"
            :navigation="{ nextEl: '.swiper-button-next', prevEl: '.swiper-button-prev' }"
            autoplay
        >
            <swiper-slide v-for="product in products" :key="product.id">
                <div class="product-card">
                    <img
                        :src="product.image"
                        :alt="product.name"
                        class="product-image"
                        loading="lazy"
                    />
                </div>
            </swiper-slide>
        </swiper>
        <div class="swiper-button-next"></div>
        <div class="swiper-button-prev"></div>
    </div>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/swiper-bundle.css';

export default {
    name: 'BannerSlider',
    components: {
        Swiper,
        SwiperSlide
    },
    data() {
        return {
            products: [
                {
                    id: 1,
                    name: 'Product 1',
                    image: '/images/banners/banner_1.jpg',
                },
                {
                    id: 2,
                    name: 'Product 2',
                    image: '/images/banners/banner_2.jpg',
                },
                {
                    id: 3,
                    name: 'Product 3',
                    image: '/images/banners/banner_3.jpg',
                }
            ],
            slidesPerView: 1,
        };
    },
};
</script>

<style scoped>
    .product-slider {
        width: 100%;
        margin: 20px auto;
    }

    .product-card {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        background-color: #fff;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.1);
        border-radius: 8px;
        overflow: hidden;
    }

    .product-image {
        width: 100%;
        height: auto;
    }

    .product-name {
        font-size: 1.2rem;
        font-weight: bold;
        margin: 0.5rem 0;
    }

    .product-price {
        font-size: 1rem;
        color: #888;
    }

    .swiper-button-next,
    .swiper-button-prev {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        width: 50px;
        height: 50px;
        background-color: rgba(0, 0, 0, 0.7);
        color: #fff;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        z-index: 10;
    }

    .swiper-button-next {
        display: none;
        right: 10px;
    }

    .swiper-button-prev {
        display: none;
        left: 10px;
    }

    .swiper-button-next::after,
    .swiper-button-prev::after {
        font-size: 24px;
        font-weight: bold;
    }

    @media (max-width: 768px) {
        .swiper-button-next,
        .swiper-button-prev {
            width: 40px;
            height: 40px;
        }

        .swiper-button-next::after,
        .swiper-button-prev::after {
            font-size: 20px;
        }
    }
</style>
