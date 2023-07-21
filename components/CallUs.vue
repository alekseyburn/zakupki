<template>
  <section id="call" class="call">
    <div class="container">
      <div class="call__container">
        <p class="call__text">
          Стать нашим клиентом очень просто. Для этого вы можете отправить запрос на коммерческое
          предложение, либо на выставление счета. Вам необходимо лишь позвонить нам по телефону или
          отправить электронное письмо, и мы постараемся оперативно рассмотреть вашу заявку.
          Надеемся, что мы сможем установить с вами прочные, долговременные и взаимовыгодные
          отношения, как и с другими нашими многочисленными клиентами
        </p>
        <div class="call__form-container">
          <div class="call__action">
            <div class="arrow" />
            <h2 class="call__title">
              Закажите звонок
            </h2>
            <p class="call__description">
              Оставьте заявку, наши специалисты свяжутся с вами и ответят на все вопросы
            </p>
          </div>
          <form action="" class="call__form">
            <input class="call__input" placeholder="Ваше имя" type="text">
            <input class="call__input" placeholder="Ваш номер" type="number">
            <input class="call__input" placeholder="Ваш e-mail" type="email">
            <p class="call__agreement">
              Нажимая на кнопку , я соглашаюсь на обработку персональных данных
            </p>
            <button class="button call__button">
              Отправить
            </button>
          </form>
        </div>
      </div>
    </div>
  </section>
</template>

<style lang="scss">
.call {
  background-image: url("/bg-call.jpg");
  background-repeat: no-repeat;
  background-position: right center;
  background-size: cover;
  padding-block: 60px;

  &__container {
    display: grid;
    max-width: 880px;
    row-gap: 48px;
  }

  &__text {
    font-weight: 500;
    padding-inline: 60px;
  }

  &__form-container {
    display: flex;
    padding: 40px 34px;
    border-radius: 20px;
    column-gap: 20px;
    background-color: $main-bg;
  }

  &__action {
    position: relative;
    z-index: 1;
    max-width: 320px;
    padding: 35px 24px;
    border: 2px solid $orange-600;
    border-radius: 20px;
    background-color: $white;
  }

  .arrow {
    position: absolute;
    inset: auto auto 15px -15px;
    z-index: -1;
    border-top: solid 40px transparent;
    border-bottom: solid 40px transparent;
    border-left: solid 50px $orange-600;
    transform: rotate(90deg);

    &::before,
    &::after {
      position: absolute;
      content: '';
    }

    &::before {
      inset: -40px 0 auto auto;
      width: 50px;
      height: 50px;
      background-color: $white;
    }

    &::after {
      inset: -40px auto auto -48px;
      border-top: solid 36px transparent;
      border-bottom: solid 40px transparent;
      border-left: solid 50px $white;
    }
  }

  &__title {
    margin-bottom: 22px;
    color: $alter-text;
    font-size: 30px;
  }

  &__description {
    color: $alter-text;
    font-size: 17px;
    line-height: 20px;
  }

  &__form {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }

  &__input {
    padding: 15px 22px;
    border-radius: 6px;
    color: $alter-text;
    font-size: 17px;
    line-height: 20px;
    background: rgba(0, 9, 60, 0.10);

    &:first-child {
      grid-column: 1 / -1;
    }
  }

  &__agreement {
    align-self: center;
    justify-self: center;
    width: 176px;
    color: $alter-text;
    font-size: 10px;
    line-height: 12px;
  }

  &__button {
    font-size: 17px;
    line-height: 20px;
    padding-block: 15px;
  }
}
</style>
