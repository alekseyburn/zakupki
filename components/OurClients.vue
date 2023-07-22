<script setup>
const clients = [
  { title: 'ММБУ «Управление дорожного хозяйства»', img: '/client-1.png' },
  { title: 'МБУ «Никельская дорожная служба»', img: '/client-2.png' },
  { title: 'ГАПОУ МО «Мурманский индустриальный колледж»', img: '/client-3.png' },
  { title: 'ГАПОУ МО «Кольский транспортный колледж»', img: '/client-4.png' },
  { title: 'ГОБУМП «Региональный центр патриотического воспитания и допризывной подготовки молодежи»', img: '/client-5.png' },
]
</script>

<template>
  <client-only>
    <section class="clients container">
      <h2 class="clients__title">
        Наши клиенты
      </h2>
      <ul class="clients__list">
        <li v-for="(client, idx) of clients" :key="idx" class="clients__item">
          <div class="clients__picture">
            <img :src="client.img" alt="" loading="lazy">
          </div>
          <p class="clients__name">
            {{ client.title }}
          </p>
        </li>
      </ul>
    </section>
  </client-only>
</template>

<style lang="scss">
.clients {
  padding-block: 55px;

  &__title {
    text-align: center;
    margin-bottom: 45px;
    color: $accent-text;
    font-size: 35px;
    line-height: 40px;
  }

  &__list {
    display: grid;
    grid-auto-flow: column;
    justify-content: space-between;
    column-gap: 65px;
  }

  &__item {
    display: grid;
    justify-items: center;
  }

  &__picture {
    width: 160px;
    height: 147px;
    display: grid;
    place-content: center;
  }

  &__name {
    font-size: 14px;
    line-height: 16px;
    color: $alter-text;
    text-align: center;
  }
}
</style>
