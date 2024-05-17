<template>
  <footer>
    <div class="footer-container">
      <div class="footer-info">
        <div>
          <img src="../../imgs/MIREA_Gerb_Colour.png" alt="MIREA University Logo" class="footer-logo">
        </div>
        <div class="footer-contacts">
          <p class="address-title title">Адрес:</p>
          <p class="address text">Москва, Пр-т Вернадского, д. 78</p>
          <p class="contacts-title title">Контакты:</p>
          <p><a class="phone text" href="tel:+74996008080">+7 499 600-80-80</a></p>
          <p><a class="email text" href="mailto:rector@mirea.ru">rector@mirea.ru</a></p>
        </div>
        <div class="footer-social">
          <ul>
            <li><a href="https://vk.com/mirea_official"><img class="footer-social-logo" src="../../imgs/icons8-vkontakte-50.png" alt="VKontakte"></a></li>
            <li><a href="http://telegram.me/rtumirea_official"><img class="footer-social-logo" src="../../imgs/icons8-telegram-50.png" alt="Telegram"></a></li>
            <li><a href="https://ok.ru/rtumirea"><img class="footer-social-logo" src="../../imgs/icons8-odnoklassniki-50.png" alt="Odnoklassniki"></a></li>
            <li><a href="https://dzen.ru/rtumirea"><img class="footer-social-logo" src="../../imgs/icons8-яндекс-был-50.png" alt="Dzen"></a></li>
            <li><a href="https://rutube.ru/channel/23657936/"><img class="footer-social-logo" src="../../imgs/rutube-svgrepo-com.png" alt="Rutube"></a></li>
            <li><a href="https://www.tiktok.com/@rtu.mirea?lang=ru-RU"><img class="footer-social-logo" src="../../imgs/icons8-tiktok-50.png" alt="TikTok"></a></li>
            <li><a href="https://www.youtube.com/channel/UClVZx_AWcLq8cXViG9NSXAA"><img class="footer-social-logo" src="../../imgs/icons8-youtube-50.png" alt="YouTube"></a></li>
          </ul>
        </div>
      </div>
      <div class="footer-links">
        <ul>
          <li><a href="#" class="footer-links-text">Главная</a></li>
          <li><a href="#" class="footer-links-text">О нас</a></li>
          <li><a href="#" class="footer-links-text">Сотрудничество</a></li>
          <li><a href="#" class="footer-links-text">Новости</a></li>
          <li><a href="#" class="footer-links-text">Контакты</a></li>
        </ul>
      </div>
    </div>
    <div class="footer-bottom">
      <p class="footer-bottom-text">© 2024 Relume. All rights reserved.</p>
      <p><a class="footer-bottom-text" href="#">Privacy Policy</a></p>
      <p><a class="footer-bottom-text" href="#">Terms of Service</a></p>
      <p><a class="footer-bottom-text" href="#">Cookies Settings</a></p>
    </div>
  </footer>
</template>

<script>
export default {
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter+Tight:ital,wght@0,100..900;1,100..900&display=swap');
footer{
  background-color: #153A4B;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  width: 100%;
  margin: 0 auto;
}

.footer-container {
  max-width: 1085px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  text-align: left;
  align-items: center;
  border-color: rgba(255, 255, 255, 0.5);
  border-width: 2px;
  border-style: solid;
  margin: 80px auto 32px auto;
  padding: 30px 70px 30px 70px;
}

.footer-logo{
  height: 120px;
}

.footer-contacts{
  margin-top: 32px;
}

.title{
  font-size: 16px;
  font-family: "Inter Tight", sans-serif;
  font-weight: 400;
  color: white;
}

.contacts-title{
  margin-top: 24px;
}

.text{
  font-size: 16px;
  font-family: "Inter Tight", sans-serif;
  font-weight: 200;
  color: white;
}

.footer-social ul{
  display: flex;
  list-style: none;
  padding-left: 0;
}

.footer-social li{
  margin-right: 12px;
}

.footer-social-logo{
  height: 24px;
}

.footer-links li{
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}

.footer-links-text{
  text-decoration: none;
  color: white;
  font-size: 16px;
  font-family: "Inter Tight", sans-serif;
  font-weight: 400;
}

.footer-bottom{
  max-width: 1220px;
  width: 100%;
  display: flex;
  justify-content: space-between;
  margin-bottom: 50px;
}

.footer-bottom > *:nth-child(2){
  margin-left: 15em;
}

.footer-bottom-text{
  color: white;
  font-size: 16px;
  font-family: "Inter Tight", sans-serif;
  font-weight: 400;
}

@media (max-width: 1300px) {
  .footer-container {
    width: 80%;
    margin: 80px 20px 32px 20px;
  }
  .footer-bottom {
    width: 90%;
  }
  .footer-bottom > *:nth-child(2){
    margin-left: 0;
  }
}

@media (max-width: 430px) {
  .footer-container{
    flex-direction: column;
    padding: 0;
    text-align: center;
  }
  .footer-links{
    display: none;
  }
  .footer-info div img{
    margin-top: 25px;
  }
}
</style>
