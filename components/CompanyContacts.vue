<template>
  <section id="contacts" class="contacts container">
    <div class="contacts__map">
      <div class="contacts__iframe" style="overflow:hidden;">
        <a
          href="https://yandex.ru/maps/23/murmansk/?utm_medium=mapframe&utm_source=maps"
          style="color:#eee;font-size:12px;position:absolute;top:0;"
        >
          Murmansk
        </a>
        <a
          href="https://yandex.ru/maps/23/murmansk/house/domostroitelnaya_ulitsa_9/Z0oYdwZoS0IHQFhifXV4eX9hbA==/?ll=33.118271%2C68.998328&utm_medium=mapframe&utm_source=maps&z=17"
          style="color:#eee;font-size:12px;position:absolute;top:14px;"
        >
          Domostroitelnaya Street, 9, Murmansk — YandexMaps
        </a>
        <iframe
          allowfullscreen
          height="379"
          loading="lazy"
          src="https://yandex.ru/map-widget/v1/?ll=33.118271%2C68.998328&mode=whatshere&whatshere%5Bpoint%5D=33.118270%2C68.998328&whatshere%5Bzoom%5D=17&z=17"
          style="position:relative;"
          width="705"
        />
      </div>
      <div class="div contacts__map-shadow" />
    </div>
    <div class="contacts__main">
      <h2 class="contacts__title">
        Контакты
      </h2>
      <ul class="contacts__list">
        <li class="contacts__item">
          <img alt="" class="contacts__icon" loading="lazy" src="/contact_call.svg">
          <div class="contacts__data">
            <a class="contacts__link" href="tel:+79215114441">+7 (921) 511-44-41</a>
            <a class="contacts__link" href="tel:+79969342989">+7 (996) 934-29-89</a>
          </div>
        </li>
        <li class="contacts__item">
          <img alt="" class="contacts__icon" loading="lazy" src="/contact_mail.svg">
          <div class="contacts__data">
            <a
              class="contacts__link"
              href="mailto:zakupki.andr@gmail.com"
            >zakupki.andr@gmail.com</a>
            <a class="contacts__link" href="mailto:tarasowandreyig@gmail.com">tarasowandreyig@gmail.com</a>
          </div>
        </li>
        <li class="contacts__item">
          <img alt="" class="contacts__icon" loading="lazy" src="/contact_pin.svg">
          <div class="contacts__data">
            <p class="contacts__link">
              г. Мурманск,
            </p>
            <p class="contacts__link">
              ул. Домостроительная, оф. 9
            </p>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<style lang="scss">
.contacts {
  flex-direction: row;
  column-gap: 110px;
  padding-block: 115px;

  &__map {
    position: relative;
    width: 705px;
  }

  &__iframe {
    position: absolute;
  }

  &__map-shadow {
    position: relative;
    top: 28px;
    left: 28px;
    z-index: -1;
    width: 705px;
    height: 379px;
    background: linear-gradient(344deg, #939393 0%, rgba(147, 147, 147, 0.00) 100%);
  }

  &__title {
    position: relative;
    margin-bottom: 80px;
    color: $alter-text;
    font-size: 35px;
    line-height: 40px;

    &::after {
      position: absolute;
      inset: auto 0 -26px 0;
      height: 4px;
      background-image: linear-gradient(90deg, #F28622 0%, rgba(242, 134, 34, 0.00) 100%);
      content: '';
    }
  }

  &__list {
    display: grid;
    row-gap: 40px;
  }

  &__item {
    display: flex;
    column-gap: 30px;
  }

  &__icon {
    width: 50px;
    height: 50px;
  }

  &__data {
    display: grid;
  }

  &__link {
    color: $alter-text;
    font-weight: 500;
    line-height: 24px;
  }
}
</style>
