<script setup>
import { reactive } from 'vue'

const directions = reactive([
  {
    title: 'Решения Softline',
    img: '/solutions.jpg',
    alt: 'Решения',
    text: 'ГК Softline предлагает клиентам собственную линейку оборудования (ПК, серверы, торговое оборудование и проч.), разработку программных продуктов, облачных решений, решений в области информационной безопасности.',
    hover: false
  },
  {
    title: 'Кибербезопасность',
    img: '/cyberSec.jpg',
    alt: 'Кибербезопасность',
    text: 'Softline обладает всеми необходимыми государственными лицензиями для организации проектов по информационной безопасности и аттестации. ',
    hover: false
  },
  {
    title: 'Импортозамещение',
    img: '/import.jpg',
    alt: 'Импортозамещение',
    text: 'ГК Softline обладает широчайшим портфелем решений и услуг для импортозамещения, включая ПО и оборудование собственного производства.',
    hover: false
  },
  {
    title: 'Облачные решения',
    img: '/clouds.jpg',
    alt: 'Облачные решения',
    text: 'Softline использует современные облачные решения как российских, так и международных вендоров для масштабирования бизнеса своих клиентов. Подписки, услуги, трансформация.',
    hover: false
  },
  {
    title: 'Цифровая трансформация и разработка ПО',
    img: '/develop.jpg',
    alt: 'разработка ПО',
    text: 'Softline использует современные технологи и новые возможности для увеличения производительности бизнеса заказчика. В штате ГК Softline - 2000+ разработчиков, которые трансформируют ПО под нужды конкретного предприятия.',
    hover: false
  },
  {
    title: 'Техническая поддержка Softline',
    img: '/support.jpg',
    alt: 'Техническая поддержка',
    text: '200+ инженеров, 24 часа в сутки, 7 дней в неделю, 12 месяцев в году, сервисное партнерство с 30+ мировыми производителями.',
    hover: false
  }
])

const setHover = (index, value) => {
  directions[index].hover = value
}
</script>

<template>
  <section class="directions">
    <h2 class="directions__title">Направления бизнеса</h2>
    <ul class="directions__list">
      <li
        class="directions__list-item"
        v-for="(direction, index) in directions"
        :key="index"
        @mouseover="setHover(index, true)"
        @mouseleave="setHover(index, false)"
      >
        <img class="directions__list-item_img" :src="direction.img" :alt="direction.alt" />

        <h3 class="directions__list-item_title" v-if="!direction.hover">{{ direction.title }}</h3>
        <h3 class="directions__list-item_title-hover" v-if="direction.hover">
          {{ direction.title }}
        </h3>

        <p class="directions__list-item_text" v-if="direction.hover">{{ direction.text }}</p>
      </li>
    </ul>
  </section>
</template>

<style lang="scss" scoped>
.directions {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 100px 0;
  flex-wrap: wrap;
  justify-content: space-between;

  &__title {
    color: $black;
    font-size: 56px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
    margin-bottom: 55px;
  }

  &__list {
    display: grid;

    grid-template-columns: repeat(2, 1fr);
    column-gap: 25px;
    row-gap: 22px;
    list-style-type: none;

    &-item {
      position: relative;
      width: 100%;
      overflow: hidden;
      height: 260px;
      cursor: pointer;
    }

    &-item_img {
      width: 100%;
      object-fit: cover;
      height: 100%;
    }

    &-item_title {
      width: 100%;
      color: $white;
      background-color: rgba(45, 54, 83, 0.6);

      position: absolute;
      bottom: 0px;

      padding: 28px 0 28px 20px;

      font-size: 24px;
      font-style: normal;
      font-weight: 600;
      line-height: 100%;

      &-hover {
        width: 100%;
        color: $white;
        background-color: rgba(45, 54, 83, 0.6);

        position: absolute;
        bottom: 0px;

        padding: 28px 0 28px 20px;

        font-size: 24px;
        font-style: normal;
        font-weight: 600;
        line-height: 100%;
        top: 0px;
      }
    }

    &-item_text {
      position: absolute;
      top: 50px;
      font-size: 17px;
      font-style: normal;
      font-weight: 400;
      line-height: 140%;
      color: $white;
      width: 480px;

      padding: 0 0 0 20px;
      margin-top: 20px;
    }
  }
}
</style>
