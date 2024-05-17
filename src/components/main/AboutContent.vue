<template>
  <div class="about-block">
    <div class="about-title-block">
      <div class="line"></div>
      <p class="about-title">О КОНФЕРЕНЦИИ</p>
      <div class="line"></div>
    </div>
    <p class="main-text">C 2021 года конференция - уникальная площадка междисциплинарного диалога специалистов в области
      информационной безопасности, IT, искусственного интеллекта, права, позволяющая обсудить актуальные технические и
      правовые аспекты защиты информации, эффективные способы обработки информации, снижения рисков неправомерного доступа,
      моделирования механизмов предупреждения киберинцидентов, проблемы правовой квалификации киберпреступлений и деликтов,
      профилактики девиантного и виктимного поведения.</p>
  </div>
</template>

<script>
export default {
  name: 'AboutBlock',
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter+Tight:ital,wght@0,100..900;1,100..900&display=swap');
.about-block {
  min-height: 650px;
  max-width: 1100px;
  width: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background-color: #FFFFFF;
  margin: 0 auto;
}

.about-title-block {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 50px;
  margin-top: 50px;
}

.about-title {
  color: #085578;
  font-size: 24px;
  margin: 0;
  font-family: "Inter Tight", sans-serif;
  white-space: nowrap;
}

.line {
  height: 1px;
  background-color: #085578;
  margin: 0 50px 0 50px;
  flex-grow: 1;
}

.main-text {
  color: #000000;
  font-size: 24px;
  text-align: center;
  margin: 0 50px 50px 50px;
  font-family: "Inter Tight", sans-serif;
  font-weight: 300;
}

@media (max-width: 4300px) {
  .line {
    display: none;
  }
  .main-text{
    font-size: 16px;
  }
  .about-title-block{
    margin-bottom: 15px;
  }
  .about-block{
    min-height: 580px;
  }
}
</style>
