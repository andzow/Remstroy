<script setup lang='ts'>
function start() {
    let vh = window.innerHeight * 0.01;
    document.documentElement.style.setProperty('--vh', `${vh}px`);
}

onMounted(() => {
    start()
})
</script>

<template>
    <section class="main" id="main">
        <div class="main__container">
            <h1 class="main__title" data-aos="zoom-out-up" data-aos-delay="500">Ремонт под ключ вашего пространства</h1>
            <p class="main__text" data-aos="zoom-out-up" data-aos-delay="700">Мы превращаем старые объекты в новые шедевры. Качественно, быстро и с гарантией обновим любое помещение.</p>
            <a class="main__btn" data-aos="zoom-out-up" data-aos-delay="500" href="tel:+79950684351">Оформить заказ</a>
        </div>
        <div class="main__overlay"></div>
        <video
            class="main__video"
            type="video/mp4"
            autoplay
            muted
            loop
            preload="metadata"
            playsinline
        >
      <source src="/Main/main.mp4" />
    </video>
    </section>
</template>

<style scoped lang="scss">
.main {
    width: 100%;
    height: calc(var(--vh, 1vh) * 100);
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;

    &__container {
        z-index: 3;
        color: var(--white);
        display: flex;
        flex-direction: column;
        align-items: center;
        padding: 0 20px;
    }

    &__video {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        object-fit: cover;
        height: 100%;
        z-index: 1;
    }

    &__overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.5); 
        pointer-events: none;
        z-index: 2;
    }

    &__title {
        font-size: 56px;
        font-weight: 700;
        max-width: 700px;
        line-height: 56px;
        text-align: center;
        margin-bottom: 15px;
    }

    &__text {
        font-size: 18px;
        max-width: 700px;
        text-align: center;
        margin-bottom: 10px;
    }

    &__btn {
        background: var(--red);
        display: inline-block;
        padding: 15px 25px;
        border-radius: 20px;
        font-weight: 400;
        transition: all .3s ease;
    }

    &__btn:hover {
        transform: scale(1.03);
    }

    @media(max-width: 700px) {
        &__title {
            font-size: 46px;
            line-height: 46px;
            padding-top: 70px;
        }

        &__text {
            margin-bottom: 15px;
        }
    }

    @media(max-width: 500px) {
        &__title {
            font-size: 36px;
            line-height: 36px;
        }
    }
}
</style>