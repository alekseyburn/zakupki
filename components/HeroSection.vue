<template>
  <section class="hero">
    <div class="container">
      <div class="hero__container">
        <h1 class="hero__title">
          Комплексное снабжение предприятий и организаций
        </h1>
        <p class="hero__text">
          Закажите по программе госзакупок (44, 223-ФЗ)
        </p>
        <p class="hero__text hero__text--last">
          Снабжаем предприятия - поиск, закупка и поставка с максимальной
          выгодой для вас и оплатой по одному счету
        </p>
        <a class="button" href="#call">Получить коммерческое предложение/счет</a>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.hero {
  display: grid;
  align-content: center;
  height: 100vh;
  background-image: url("/bg-head.jpg");
  background-repeat: no-repeat;
  background-position: right center;
  background-size: cover;

  &__container {
    display: grid;
    justify-items: start;
    max-width: 660px;
  }

  &__title {
    margin-bottom: 10px;
    font-weight: 700;
    font-size: 45px;
    line-height: 52px;
  }

  &__text {
    margin-bottom: 35px;
    font-weight: 500;
    font-size: 24px;
    line-height: 28px;

    &--last {
      font-weight: 400;
    }
  }
}
</style>
