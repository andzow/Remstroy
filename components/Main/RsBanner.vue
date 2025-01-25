<script setup lang='ts'>
</script>

<template>
    <section class="banner">
        <div class="banner__container">
            <h3 class="banner__name" data-aos="zoom-out-up" data-aos-delay="500">Готовы к ремонту? Получите расчет без задержек!</h3>
            <p class="banner__text" data-aos="zoom-out-up" data-aos-delay="500">Мы предлагаем профессиональные услуги по ремонту и реконструкции. Свяжитесь с нами, и мы поможем вам воплотить ваши идеи в жизнь с учетом всех ваших пожеланий.</p>
            <a class="banner__btn" href="tel:+79950684351" data-aos="zoom-out-up" data-aos-delay="500">Мы на связи!</a>
        </div>
    </section>
</template>

<style scoped lang="scss">
.banner {
    background: url('/Main/banner.webp');
    background-position: 50% 50%;
    background-size: cover;
    overflow: hidden;
    padding: 100px 0;

    &__container {
        padding: 0 20px;
        margin: 0 auto;
        max-width: 1400px;
    }

    &__name {
        font-size: 54px;
        line-height: 54px;
        max-width: 700px;
        margin-bottom: 30px;
    }

    &__text {
        max-width: 700px;
        font-size: 18px;
        margin-bottom: 20px;
    }

    &__btn {
        background: var(--red);
        display: inline-block;
        padding: 15px 25px;
        border-radius: 20px;
        font-weight: 400;
        transition: all .3s ease;
        color: var(--white);
    }

    &__btn:hover {
        transform: scale(1.03);
    }

    @media(max-width: 700px) {
        padding: 40px 0;

        &__name {
            font-size: 44px;
            line-height: 44px;
        }
    }

    @media(max-width: 560px) {
        &__name {
            font-size: 38px;
            line-height: 38px;
        }
    }
}
</style>