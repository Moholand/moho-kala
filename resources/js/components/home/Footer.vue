<template>
    <div class="footer">
        <div class="footer-logo d-flex justify-content-between w-100">
            <div class="brand d-flex align-items-center">
                <img src="/images/logos/logo.png" width="115" height="45" alt="logo"/>
                <h5 class="name">موهو کالا</h5>
            </div>
            <button class="scroll-top d-flex align-items-center" @click="scrollToTop">
               <span class="px-2">بازگشت به بالا</span>
                <i class="fa-solid fa-caret-up"></i>
            </button>
        </div>
        <div class="contact d-flex mt-4 px-3">
            <span>تلفن پشتیبانی ۶۱۶۱۶۱۶۱ - ۰۲۱</span>
            <span>|</span>
            <span>۰۲۱ - ۹۱۲۲۲۱۲۲</span>
            <span>|</span>
            <span>۷ روز هفته، ۲۴ ساعته پاسخگوی شما هستیم</span>
        </div>
        <div class="features d-flex mt-5 px-3">
            <div class="feature-item">
                <img src="/images/logos/features/express-delivery.svg" width="56" height="56" alt="express-delivery"/>
                <p>اﻣﮑﺎن ﺗﺤﻮﯾﻞ اﮐﺴﭙﺮس</p>
            </div>
            <div class="feature-item">
                <img src="/images/logos/features/cash-on-delivery.svg" width="56" height="56" alt="cash-on-delivery"/>
                <p>امکان پرداخت در محل</p>
            </div>
            <div class="feature-item">
                <img src="/images/logos/features/support.svg" width="56" height="56" alt="support"/>
                <p>۷ روز ﻫﻔﺘﻪ، ۲۴ ﺳﺎﻋﺘﻪ</p>
            </div>
            <div class="feature-item">
                <img src="/images/logos/features/days-return.svg" width="56" height="56" alt="days-return"/>
                <p>هفت روز ضمانت بازگشت کالا</p>
            </div>
            <div class="feature-item">
                <img src="/images/logos/features/original-products.svg" width="56" height="56" alt="original-products"/>
                <p>ﺿﻤﺎﻧﺖ اﺻﻞ ﺑﻮدن ﮐﺎﻟﺎ</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    methods: {
        scrollToTop() {
            window.scrollTo({
                top: 0,
                behavior: 'smooth'
            });
        },
    },
};
</script>

<style>
    .footer {
        border-top: #d5d8df 2px solid;
        padding: 40px 90px;
    }
    .brand .name {
        margin: 0;
        color: #2a909bff;
        font-weight: 500;
    }
    .scroll-top {
        color: #888a91ff;
        font-size: 12px;
        font-weight: 500px;
        border: #d5d8df 1px solid;
        border-radius: 5px;
        padding: 0 20px;
    }
    .contact {
        font-size: 13px;
        font-weight: 500;
        color: #3f4064;
    }
    .contact span {
        padding-left: 15px;
    }
    .features {
        justify-content: space-around;
    }
    .feature-item {
        display: flex;
        flex-direction: column;
        align-items: center;
        cursor: pointer;
    }
    .feature-item p {
        font-size: 12px;
        color: #3f4064;
    }
</style>
