<script setup>
const links = [
  { title: 'О компании', anchor: '#company' },
  { title: 'Преимущества', anchor: '#advantages' },
  { title: 'Заказать звонок', anchor: '#call' },
  { title: 'Контакты', anchor: '#contacts' },
]
</script>

<template>
  <header class="header">
    <nav class="header__nav">
      <a
        v-for="link of links" :key="link.anchor" :href="link.anchor"
        class="header__link"
      >
        {{ link.title }}
      </a>
    </nav>
  </header>
</template>

<style lang="scss">
.header {
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  filter: drop-shadow(0 4px 4px rgba($black, 0.25));

  &__nav {
    display: grid;
    grid-auto-flow: column;
    padding: 20px 90px;
    font-weight: 500;
    line-height: 22px;
    white-space: nowrap;
    column-gap: 40px;
    background-color: $accent-bg;
    clip-path: polygon(0 0, 100% 0, calc(100% - 62px) 62px, 62px 62px);
  }
}
</style>
