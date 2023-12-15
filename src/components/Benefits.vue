<script setup>
const benefits = [
  { text: 'ДМС', img: '/dms.svg', alt: 'дмс' },
  { text: 'Выходной в день рождения', img: '/bday.svg', alt: 'Выходной в день рождения' },
  { text: 'Корпоративная мобильная связь', img: '/cell.svg', alt: 'Корпоративная мобильная связь' },
  { text: 'Корпоративные скидки на спорт', img: '/gym.svg', alt: 'Корпоративные скидки на спорт' },
  { text: 'LTI', img: '/hands.svg', alt: 'LTI' }
]
const motivations = [
  { text: 'Оргтехники', img: '/xerox.svg', alt: 'Оргтехники' },
  { text: 'ДМС', img: '/dms.svg', alt: 'ДМС' },
  { text: 'Ипотеки', img: '/credit.svg', alt: 'Ипотеки' }
]
</script>

<template>
  <section class="benefits">
    <h2 class="benefits__title">Компенсационный пакет</h2>
    <ul class="benefits__list">
      <li class="benefits__list-item" v-for="benefit in benefits" :key="benefit">
        <img class="benefits__list-item-img" :src="benefit.img" :alt="benefit.alt" />
        <p class="benefits__list-item-text">{{ benefit.text }}</p>
      </li>
    </ul>

    <div class="benefits__line"></div>

    <h3 class="benefits__subtitle">
      Программа дополнительной мотивации
      <span class="benefits__subtitle-span">доплата 12% от суммы</span>
    </h3>
    <ul class="benefits__list">
      <li class="benefits__list-item" v-for="(motivation, index) in motivations" :key="index">
        <img class="benefits__list-item-img" :src="motivation.img" :alt="motivation.alt" />
        <p class="benefits__list-item-text">{{ motivation.text }}</p>
      </li>
    </ul>
  </section>
</template>

<style lang="scss" scoped>
.benefits {
  box-shadow: 0px 0px 40px 0px rgba(0, 0, 0, 0.06);
  margin: 0 70px 103px;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding-bottom: 80px;
 

  @media screen and (max-width: 320px) {

    padding-bottom: 50px;
    width: 100%;
  margin: 0 auto;
  }

  &__title {
    color: $black;
    font-size: 56px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
    margin: 80px 0 50px;
    @media screen and (max-width: 320px) {
      font-size: 28px;
      line-height: 100%;
      margin: 24px 0 40px;
    }
  }

  &__subtitle {
    color: $black;
    font-size: 40px;
    font-style: normal;
    font-weight: 600;
    line-height: 120%;
    display: flex;
    flex-direction: column;
    align-items: center;
    margin-bottom: 50px;

    @media screen and (max-width: 320px) {
      font-size: 28px;
      line-height: 100%;
      text-align: center;
      margin-bottom: 25px;
      
    }

    &-span {
      color: $red;

    }
  }

  &__line {
    width: 90%;
    height: 1px;
    background-color: $black;
    opacity: 0.1;
    margin: 75px 0 70px;

    @media screen and (max-width: 320px) {
      margin: 24px 0;
    }
  }

  &__list {
    list-style: none;
    display: flex;
    justify-content: space-between;
    gap: 16px;
    flex-wrap: wrap;
    

    &-item {
      display: flex;
      flex-direction: column;
      align-items: center;
      gap: 10px;
      width: 178px;
      flex: 1 0 45%;

      @media screen and (max-width: 320px) {
        width: 120px;
      }

      &-img {
        border-radius: 50%;
        background-color: $black;

        width: 110px;
        height: 110px;
        object-fit: contain;
        background-color: rgba(0, 0, 0, 0.1);

        @media screen and (max-width: 320px) {
          width: 80px;
          height: 80px;
        }
      }

      &-text {
        font-size: 18px;
        font-style: normal;
        font-weight: 400;
        line-height: 110%;
        color: $black;
        text-align: center;
      }
    }
  }
}
</style>
