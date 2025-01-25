<script setup>
const route = useRoute();
const router = useRouter();

function scrollToTop () {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
    })
}

function scrollToAnchor(anchorMain) {
  if (route.name === "index") {
    const anchor = document.getElementById(anchorMain);
    if (anchor) {
      const offset = 90;
      const top = anchor.getBoundingClientRect().top + window.scrollY - offset;
      window.scrollTo({ top, behavior: 'smooth' });
    }
  } else {
    const newRoute = { path: '/', hash: `#${anchorMain}`};
    router.push(newRoute);
  }
}
</script>


<template>
  <header class="header">
    <div class="header__container">
      <h2 class="header__logo">Рем<span class="header__span">строй</span></h2>
      <nav class="header__position">
        <ul class="header__nav">
          <li @click="scrollToAnchor('main')" class="header__item">Главная</li>
          <li @click="scrollToAnchor('company')" class="header__item">Компания</li>
          <li @click="scrollToAnchor('services')" class="header__item">Услуги</li>
          <li @click="scrollToAnchor('blog')" class="header__item">Блог</li>
        </ul>
        <a class="header__btn" href="tel:+79950684351">Позвонить</a>
      </nav>
    </div>
  </header>
</template>

<style scoped lang="scss">
.header {
  position: fixed;
  padding: 35px 0;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 50;
  background: rgba(0, 0, 0, .4);
  backdrop-filter: blur(15px);

  &__container {
  padding: 0 20px;
  margin: 0 auto;
  max-width: 1700px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

&__nav {
  display: flex;
  align-items: center;
  color: var(--white);
  margin-left: 70px;
}

&__position {
    display: flex;
    align-items: center;
}

&__item {
  cursor: pointer;
  padding-bottom: 3px;
  font-size: 18px;
  transition: all .3s ease;
  position: relative;
  font-weight: 500;
}

&__item:hover {
  color: var(--red);
  transform: translateY(-3px);
}

&__item:not(:last-child) {
  margin-right: 30px;
}

&__item:after {
  content: "";
  display: block;
  position: absolute;
  right: 0;
  bottom: -3px;
  width: 0;
  height: 2px;
  background-color: var(--red);
  transition: width 0.5s;
}

&__item:hover:after {
  content: "";
  width: 100%;
  display: block;
  position: absolute;
  left: 0;
  bottom: -3px;
  height: 2px;
  background-color: var(--red);
  transition: width 0.5s;
  font-weight: 500;
}

&__logo {
  color: var(--white);
  font-weight: 700;
  font-size: 24px;
}

&__span {
  color: var(--red);
  font-weight: 700;
}

&__btn {
    background: var(--red);
    display: inline-block;
    padding: 15px 25px;
    border-radius: 20px;
    font-weight: 400;
    transition: all .3s ease;
    color: var(--white);
    margin-left: 20px;
}

&__btn:hover {
    transform: scale(1.03);
}

@media(max-width: 780px) {
  padding: 20px 0;

  &__nav {
    display: none;
  }

  &__logo {
    font-weight: 700;
    font-size: 24px;
  }
}
}

</style>