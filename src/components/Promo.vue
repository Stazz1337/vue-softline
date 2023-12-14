<template>
  <div class="promo">
    <div class="promo__wrapper">
      <h1 class="promo__title">Поставщик услуг цифровой трансформации и&nbsp;кибербезопасности</h1>
      <a class="promo__link" target="_blank" href="https://softline.ru">Наш сайт</a>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.promo {
  color: $black;
  width: 100%;
  height: 600px;
  background-image: url('/promo.jpg');
  display: flex;
  align-items: center;

  &__wrapper {
    display: flex;
    flex-direction: column;
    gap: 60px;
    margin-left: 70px;
  }

  &__title {
    width: 709px;
    font-size: 56px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
    margin: 0;
  }

  &__link {
    display: flex;
    align-items: center;
    justify-content: center;
    text-decoration: none;
    cursor: pointer;

    background-color: $red;
    border-radius: 8px;
    color: $white;
    font-size: 18px;
    font-style: normal;
    font-weight: 600;
    line-height: 20px;
    width: 110px;
    height: 56px;

    &:hover {
      opacity: 0.8;
    }
  }
}
</style>
