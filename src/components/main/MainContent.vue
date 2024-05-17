<template>
  <div class="main-block">
    <div class="content">
      <div class="logo">
        <img src="../../imgs/MIREA_Gerb_Colour.png" alt="Company Logo" height="120">
      </div>
      <p class="event-title">КИБЕРБЕЗОПАСНОСТЬ: ТЕХНИЧЕСКИЕ И ПРАВОВЫЕ АСПЕКТЫ ЗАЩИТЫ ИНФОРМАЦИИ
      </p>
      <div class="event-info">
        <div class="info-item">
          <img src="../../imgs/icons8-календарь-48.png" alt="Calendar Icon" class="icon">
          <p>23.04.2024</p>
        </div>
        <div class="info-item">
          <img src="../../imgs/icons8-часы-48.png" alt="Clock Icon" class="icon">
          <p>10:00 – 13:15</p>
        </div>
        <div class="info-item">
          <img src="../../imgs/icons8-место-48.png" alt="Location Icon" class="icon">
          <p>г. Москва, ул. Стромынка, 20, Малый зал Учёного Совета</p>
        </div>
      </div>
    </div>
    <div class="cover"></div>
  </div>
</template>

<script>
export default {
  name: 'MainBlock'
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter+Tight:ital,wght@0,100..900;1,100..900&display=swap');
.main-block {
  position: relative;
  height: 746px;
  background-image: url('../../imgs/1643585269_15-phonoteka-org-p-kiberbezopasnost-fon-22.jpg');
  overflow: hidden;
  border-radius: 0 0 40px 40px;
  box-shadow: 0 10px 30px 0 #153A4B;
}

.cover{
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: #153A4B;
  z-index: 1;
  opacity: 0.9;
}

.content {
  position: relative;
  z-index: 2;
  height: calc(100% - 90px);
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 90px;
}

.logo {
  /*padding-top: 40px;*/
  text-align: center;
}

.event-title {
  max-width: 1000px;
  color: white;
  font-size: 70px;
  text-align: center;
  justify-content: center;
  margin: 18px 0 36px 0;
  font-weight: bold;
  line-height: 1.1;
  font-family: "Inter Tight", sans-serif;
}

.event-info {
  max-height: 220px;
  width: 100%;
  /*margin-top: 25px;*/
  display: flex;
  justify-content: center;
  align-items: center;
}

.info-item {
  display: flex;
  align-items: center;
  color: white;
  margin: 0 40px;
}

.info-item img {
  width: 25px;
  height: 25px;
}

.info-item p{
  margin-left: 10px;
  font-family: "Inter Tight", sans-serif;
  font-size: 20px;
  font-weight: normal;
}

@media (max-width: 1300px) {
  .event-title{
    max-width: 800px;
  }
  .event-info{
    width: calc(100% - 90px);
  }
}


@media (max-width: 450px) {
  .event-title{
    font-size: 26px;
    max-width: 400px;
    margin-bottom: 50px;
  }
  .event-info{
    flex-direction: column;
    max-height: 300px;
  }
  .info-item p{
    margin-left: 0;
    font-size: 16px;
    text-align: center;
    margin-top: 15px;
    margin-bottom: 30px;
  }
  .info-item{
    flex-direction: column;
  }
  .main-block{
    box-shadow: 0 5px 15px 0 #153A4B;
  }
}
</style>