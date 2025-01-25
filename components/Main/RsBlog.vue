<script setup>
</script>

<template>
    <section class="blog" id="blog">
        <div class="blog__container">
            <div class="blog__position">
                <div class="blog__image" data-aos="zoom-out-up" data-aos-delay="500">
                    <img class="blog__img" src="/Main/blog_1.webp" alt="">
                    <div class="blog__line"></div>
                </div>
                <div class="blog__info">
                    <h2 class="blog__title" data-aos="zoom-out-up" data-aos-delay="500">/блог</h2>
                    <p class="blog__name" data-aos="zoom-out-up" data-aos-delay="500">Тренды и инновации в строительстве 2025 года</p>
                    <p class="blog__text" data-aos="zoom-out-up" data-aos-delay="500">Строительная отрасль постоянно развивается, и 2025 год принесет новые тренды и технологии. В этом году особенно актуальными станут экологичные материалы, энергоэффективные решения и использование умных технологий в строительстве. В нашем блоге мы расскажем о том, какие новшества помогут улучшить качество и устойчивость построенных объектов, а также как они могут снизить эксплуатационные расходы. Следите за новыми тенденциями и будьте в курсе последних инноваций в строительстве!</p>
                </div>
            </div>

            <div class="blog__position blog__position_reverse">
                <div class="blog__image blog__image_reverse" data-aos="zoom-out-up" data-aos-delay="500">
                    <img class="blog__img" src="/Main/blog_2.webp" alt="">
                    <div class="blog__line"></div>
                </div>
                <div class="blog__info">
                    <p class="blog__name" data-aos="zoom-out-up" data-aos-delay="500">Истории успешных ремонтов и реконструкций</p>
                    <p class="blog__text" data-aos="zoom-out-up" data-aos-delay="500">Каждый проект — это уникальная история, и мы гордимся тем, что наши клиенты остаются довольны результатом. В этом разделе мы расскажем о самых интересных и нестандартных ремонтах, которые мы выполнили. От реставрации исторических зданий до создания современных интерьеров — каждый случай требует индивидуального подхода. Поделимся с вами подробностями наших успешных проектов и покажем, как мы решаем самые сложные задачи, чтобы каждый объект стал не только красивым, но и удобным для жизни или работы.</p>
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped lang="scss">
.blog {
    padding-top: 120px;
    padding-bottom: 120px;

    &__container {
        padding: 0 20px;
        margin: 0 auto;
        max-width: 1400px;
    }

    &__position {
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    &__position_reverse {
        flex-direction: row-reverse;
        margin-top: 60px;
    }

    &__image {
        position: relative;
        margin-right: 30px;
    }

    &__image_reverse {
        margin-right: 0px;
        margin-left: 30px;
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

    @media(max-width: 1000px) {
        padding-top: 80px;
        padding-bottom: 80px;

        &__position {
            flex-direction: column-reverse;
        }

        &__image {
            margin-right: 0;
            margin-top: 40px;
        }

        &__image_reverse {
            margin-left: 0;
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

        &__text {
            text-align: left;
        }
    }
}
</style>