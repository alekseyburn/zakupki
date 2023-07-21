<script setup>
const advantages = [
  {
    title: 'Профессиональная консультация',
    text: 'Специалисты нашей компании всегда применяют индивидуальный подход к каждому клиенту, готовы предоставить информацию о любом товаре, ответить на все интересующие вопросы и оказать помощь в выборе продукции.',
  },
  {
    title: 'Оперативность',
    text: 'Выполнение любых заявок по вашему профилю в кратчайшие сроки, поэтому вам больше не придётся тратить время и силы на поиск и получение необходимого товара по десяткам поставщиков, что позволит сэкономить значительные средства на транспортных и других накладных расходах.',
  },
  {
    title: 'Гарантийные обязательства',
    text: 'Работаем на основе долгосрочных партнёрских отношений и лишь с теми, кто может предоставить качественный товар, что позволяет обеспечить конкурентоспособные цены, максимальное выполнение комплексных заявок, гарантированное сертификатами качества и сервисное обслуживание.',
  },
]
</script>

<template>
  <section id="advantages" class="advantages">
    <div class="advantages__left" />
    <div class="advantages__goal">
      <h2 class="advantages__title">
        Преимущества
      </h2>
      <div class="advantages__images">
        <img alt="" height="200" loading="lazy" src="/goal_img1.jpg" width="200">
        <img alt="" height="200" loading="lazy" src="/goal_img2.jpg" width="200">
      </div>
      <div class="advantages__text-container">
        <p class="advantages__text">
          Наша главная цель – не продажа, а оптимальное решение,
          удовлетворяющее обе стороны. Мы подбираем и предлагаем оборудование в строгом
          соответствии с техническими требованиями и финансовыми возможностями заказчика, стремясь
          достичь идеального соотношения цена/качество.
        </p>
        <p class="advantages__text">
          Наши преимущества – это клиентоориентированность,
          оперативность, репутация, надёжность, широчайший ассортимент, конкурентоспособные
          цены.
        </p>
      </div>
    </div>
    <ul class="advantages__list">
      <li v-for="item of advantages" :key="item.title" class="advantages__item">
        <h3 class="advantages__subtitle">
          {{ item.title }}
        </h3>
        <p class="advantages__subtext">
          {{ item.text }}
        </p>
      </li>
    </ul>
    <div class="advantages__right" />
  </section>
</template>

<style lang="scss">
.advantages {
  display: grid;
  grid-template-columns: 1fr calc(1440px - 630px) 630px 1fr;

  &__left {
    background-color: $alter-bg;
  }

  &__right {
    background-color: $second-bg;
  }

  &__goal {
    position: relative;
    z-index: 1;
    padding: 120px 90px 130px 240px;
    background-color: $alter-bg;

    &::after,
    &::before {
      position: absolute;
      content: '';
    }

    &::after {
      inset: 0 auto 50px 0;
      border-top: 530px solid #EF7F1B;
      border-right: 240px solid transparent;
    }

    &::before {
      inset: auto auto 0 0;
      border-right: 240px solid transparent;
      border-bottom: 530px solid #B1581E;
    }
  }

  &__title {
    position: relative;
    margin-bottom: 80px;
    font-size: 35px;
    line-height: 40px;

    &::after {
      position: absolute;
      right: 0;
      bottom: 0;
      width: 640px;
      height: 11px;
      margin-bottom: -20px;
      background-image: linear-gradient(90deg, #F28622 0%, transparent 100%);
      content: '';
    }
  }

  &__images {
    display: flex;
    margin-bottom: 60px;
    column-gap: 70px;

    img {
      width: 200px;
      height: 200px;
    }
  }

  &__text-container {
    position: relative;
    display: grid;
    row-gap: 24px;

    &::before {
      position: absolute;
      top: 0;
      bottom: 0;
      width: 2px;
      background-color: $white;
      content: '';
    }
  }

  &__text {
    padding-left: 32px;
    font-size: 17px;
    line-height: 20px;
  }

  &__list {
    display: grid;
    padding: 65px 135px 35px 155px;
    background-color: $second-bg;
    row-gap: 52px;
  }

  &__item {
    position: relative;

    &::before {
      position: absolute;
      top: -20px;
      left: -200px;
      z-index: 0;
      width: 188px;
      color: #E3E3E3;
      font-weight: 700;
      font-size: 150px;
      line-height: 170px;
    }

    &:first-child::before {
      content: '01';
    }

    &:nth-child(2)::before {
      content: '02';
    }

    &:nth-child(3)::before {
      content: '03';
    }
  }

  &__subtitle {
    position: relative;
    margin-bottom: 32px;
    color: $alter-text;
    font-size: 26px;

    &::after {
      position: absolute;
      inset: auto 0 0 0;
      height: 5px;
      margin-bottom: -16px;
      background-color: #F28622;
      content: '';
    }
  }

  &__subtext {
    color: $alter-text;
    font-size: 15px;
    line-height: 18px;
  }

}
</style>
