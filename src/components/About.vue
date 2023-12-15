<script setup>
const items = [
  { title: '>30 лет', text: 'на IT-рынке' },
  { title: '4600', text: 'сотрудников в России' },
  { title: '25', text: 'городов России' },
  { title: '2000+', text: 'разработчиков' },
  { title: '3000+', text: 'сотрудников ежегодно <br /> проходят оценку и обучение' }
]
</script>

<template>
  <section class="about">
    <div class="about__wrapper">
      <p class="about__text">
        <span class="about__span"> Softline </span>
        – ведущий поставщик IT-решений и сервисов.* Мы&nbsp;предлагаем комплексные IT-решения,
        облака, программное и&nbsp;аппаратное обеспечение, решения по цифровой трансформации
        и&nbsp;кибербезопасности, а также широкий спектр IT-услуг.
      </p>
    </div>

    <div class="about__numbers">
      <div v-for="(item, index) in items" :key="index" class="about__numbers-item">
        <h2 class="about__numbers-item_title">{{ item.title }}</h2>
        <p class="about__numbers-item_text" v-html="item.text"></p>
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.about {
  padding: 100px 70px;
  margin: auto;
  @media screen and (max-width: 320px) {
    padding: 50px 0;
  }

  &__text {
    margin: 0;
    color: $black;
    padding: 100px 110px;
    text-align: center;
    font-size: 32px;
    font-style: normal;
    font-weight: 600;
    line-height: 120%;
    box-shadow: 0px 0px 32px 0px rgba(0, 0, 0, 0.08);
    @media screen and (max-width: 320px) {
      font-size: 16px;
      font-style: normal;
      font-weight: 600;
      line-height: 120%;
      padding: 24px 0;
    }
  }

  &__span {
    color: $red;
  }

  &__numbers {
    margin-top: 100px;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    column-gap: 185px;
    row-gap: 80px;

    @media screen and (max-width: 320px) {
      column-gap: 8px;
      row-gap: 24px;
      margin-top: 50px;
      
    }
  }

  &__numbers-item_title {
    color: $burgundy;
    font-size: 80px;
    font-style: normal;
    font-weight: 600;
    line-height: 80%;
    margin: 0;

    @media screen and (max-width: 320px) {
      font-size: 40px;
      font-style: normal;
      font-weight: 600;
      line-height: 80%;
      text-align: center;
    }
  }

  &__numbers-item_text {
    color: $black;
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: 150%;
    margin: 0;
    white-space: pre-wrap;

    @media screen {
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 150%;
    }
  }
}
</style>
