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
  background-repeat: no-repeat;
  background-position: cover;
  background-size: 100% 100%; 

  display: flex;
  align-items: center;

  @media screen and (max-width: 320px) {
    height: 300px;
    
  }

  &__wrapper {
    display: flex;
    flex-direction: column;
    gap: 60px;
    margin-left: 70px;

    @media screen and (max-width: 320px) {
      margin-left: 0;
      gap: 20px;
      
    }
  }

  &__title {
    width: 709px;
    font-size: 56px;
    font-style: normal;
    font-weight: 600;
    line-height: 100%;
    margin: 0;

    @media screen and (max-width: 320px) {
      font-size: 28px;
      font-style: normal;
      font-weight: 600;
      line-height: 100%; 
      width: 100%;
    }
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

    @media screen and (max-width: 320px) {
      height: 32px;
      font-size: 16px;
    }
  }
}
</style>
