<template>
  <footer class="footer">
    <div class="footer__container container">
      <div class="footer__left">
        ИП Тарасов Андрей Игоревич <br>
        ИНН 519098976314<br>
        ОГРН 321519000027453
      </div>
      <div class="footer__right">
        Юр. адрес: РФ, 183031, Мурманская <br>
        обл., г. Мурманск, ул. Шестой <br>
        Комсомольской Батареи, д. 45, кв. 8
      </div>
    </div>
  </footer>
</template>

<style lang="scss">
.footer {
  position: relative;
  font-size: 16px;
  line-height: 24px;
  background-image: url('/bg-footer.jpg');
  background-position: center center;
  background-size: cover;
  padding-block: 25px;

  &::after {
    position: absolute;
    bottom: 0;
    left: 50%;
    width: 300px;
    height: 32px;
    background-image: url('/footer-shape.png');
    transform: translateX(-50%);
    content: '';
  }

  &__container {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }

  &__right {
    text-align: right;
  }
}
</style>
