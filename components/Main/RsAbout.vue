<script setup>
const company = ref([
    {
        number: '350',
        title: 'Успешных проектов'
    },
    {
        number: '12',
        title: 'Лет непрерывной работы'
    },
    {
        number: '400',
        title: 'Довольных клиентов'
    },
])
</script>

<template>
    <section class="about" id="company">
        <div class="about__container">
            <div class="about__image" data-aos="zoom-out-up" data-aos-delay="500">
                <img class="about__img" src="/Main/about.webp" alt="">
                <div class="about__line"></div>
            </div>
            <div class="about__info">
                <h2 class="about__title" data-aos="zoom-out-up" data-aos-delay="500">/О компании</h2>
                <p class="about__name" data-aos="zoom-out-up" data-aos-delay="500">Команда надежных и опытных подрядчиков</p>
                <p class="about__text" data-aos="zoom-out-up" data-aos-delay="500">Мы специализируемся на ремонте и реконструкции жилых и коммерческих объектов. Наша команда гарантирует высококачественное выполнение работ, внимание к деталям и полное удовлетворение потребностей клиента. Независимо от того, требуется обновление помещений или выполнение текущих ремонтов, мы обеспечиваем выполнение проекта в срок и на высоком уровне.</p>
                <div class="about__position">
                    <div class="about__item" v-for="(item, idx) in company" :key="idx" data-aos="zoom-out-up" data-aos-delay="500">
                        <p class="about__number">
                            <span class="about__span">+</span>{{ item.number }}
                        </p>
                        <p class="about__slogan">{{ item.title }}</p>
                    </div>
                </div>
                <a class="about__btn" href="tel:+79950684351" data-aos="zoom-out-up" data-aos-delay="500">Узнать больше</a>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.about {
    padding-top: 120px;
    overflow: hidden;

    &__container {
        padding: 0 20px;
        margin: 0 auto;
        max-width: 1400px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    &__image {
        position: relative;
        margin-right: 30px;
    }

    &__img {
        width: 100%;
        height: 100%;
        object-fit: cover;
    }

    &__line {
        position: absolute;
        top: -10px;
        left: -10px;
        width: 200px;
        height: 200px;
        border: 3px solid var(--red);
    }

    &__title {
        font-size: 20px;
        font-weight: 600;
        text-transform: uppercase;
        color: var(--red);
        margin-bottom: 20px;
    }

    &__name {
        font-size: 54px;
        line-height: 54px;
        max-width: 700px;
        margin-bottom: 25px;
    }

    &__text {
        max-width: 700px;
        font-size: 18px;
        text-align: justify;
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

    &__position {
        display: flex;
        align-items: center;
        justify-content: space-between;
        margin-bottom: 20px;
        gap: 20px;
    }

    &__item {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    &__number {
        font-size: 56px;
        font-weight: 600;
    }

    &__span {
        color: var(--red);
    }

    @media(max-width: 1000px) {
        padding-top: 80px;

        &__container {
            flex-direction: column-reverse;
        }

        &__image {
            margin-right: 0;
            margin-top: 40px;
        }

        &__info {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        &__title {
            width: 100%;
        }
    }

    @media(max-width: 700px) {
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

        &__position {
            flex-direction: column;
        }

        &__text {
            text-align: left;
        }
    }
}
</style>