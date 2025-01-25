<script setup lang='ts'>
const services = ref([
    {
        image: '/Main/services_1.png',
        name: 'Планирование проектов',
        description: 'Мы помогаем на всех этапах планирования, от концептуальных идей до разработки подробных чертежей, обеспечивая успешное выполнение проектов.'
    },
    {
        image: '/Main/services_2.png',
        name: 'Управление проектами',
        description: 'Наши опытные менеджеры обеспечат своевременное завершение проекта, координируя все этапы, от начала до конца, с высоким качеством.'
    },
    {
        image: '/Main/services_3.png',
        name: 'Общие подрядные работы',
        description: 'Мы берем на себя все аспекты строительных и ремонтных работ, предлагая полный спектр услуг для успешной реализации проектов.'
    },
    {
        image: '/Main/services_4.png',
        name: 'Дизайн интерьеров',
        description: 'Создаем уникальные и функциональные интерьерные решения, которые отражают стиль и потребности наших клиентов, обеспечивая комфорт и эстетику.'
    },
    {
        image: '/Main/services_5.png',
        name: 'Дизайн экстерьеров',
        description: 'Разрабатываем дизайн фасадов и внешней среды, который сочетает красоту и функциональность, улучшая внешний вид и ценность вашего объекта.'
    },
    {
        image: '/Main/services_6.png',
        name: 'Планировка пространства',
        description: 'Оптимизируем использование пространства, создавая удобные и практичные решения, которые обеспечивают максимальную эффективность использования.'
    }
])
</script>

<template>
    <section class="services" id="services">
        <div class="services__container">
            <h2 class="services__title" data-aos="zoom-out-up" data-aos-delay="500">/Наши услуги</h2>
            <p class="services__name" data-aos="zoom-out-up" data-aos-delay="500">Выбор, который вдохновляет вас</p>
            <div class="services__grid">
                <div class="services__item" v-for="item in services" :key="item.name" data-aos="zoom-out-up" data-aos-delay="500">
                    <img class="services__img" :src="item.image" alt="">
                    <h3 class="services__forename">{{ item.name }}</h3>
                    <p class="services__description">{{ item.description }}</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.services {
    padding-top: 120px;
    padding-bottom: 120px;
    overflow: hidden;

    &__container {
        padding: 0 20px;
        margin: 0 auto;
        max-width: 1400px;
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
        margin-bottom: 60px;
    }

    &__grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 25px;
    }

    &__img {
        margin-bottom: 30px;
    }

    &__forename {
        font-size: 28px;
        line-height: 28px;
        font-weight: 600;
        margin-bottom: 20px;
    }

    @media(max-width: 1000px) {
        padding-top: 80px;
        padding-bottom: 80px;

        &__grid {
            grid-template-columns: repeat(2, 1fr);
        }
    }

    @media(max-width: 700px) {
        &__name {
            font-size: 44px;
            line-height: 44px;
        }

        &__grid {
            grid-template-columns: repeat(1, 1fr);
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