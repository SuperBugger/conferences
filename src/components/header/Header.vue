<template>
  <header :class="{'sticky': isSticky}" class="header">
    <div class="container">
      <div class="logo-container">
        <a href="#">
          <img src="../../imgs/MIREA_Gerb_Colour.png" class="logo_img">
        </a>
      </div>
      <nav class="nav-links">
        <ul>
          <li class="scroll_btn"><button @click="scrollTo('themes')">Программа</button></li>
          <li class="scroll_btn"><button @click="scrollTo('members')">Участники</button></li>
          <li>
            <button @click="downloadFile" class="download-file-btn">
              <img src="../../imgs/icons8-download-48.png" alt="Download Icon" class="download-file-img">
              <span class="download-file-txt">Скачать файл</span>
            </button>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      isSticky: false
    };
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      if (window.pageYOffset > 0 && !this.isSticky) {
        this.isSticky = true;
      } else if (window.pageYOffset === 0 && this.isSticky) {
        this.isSticky = false;
      }
    },
    scrollTo(elementId) {
      const element = document.getElementById(elementId);
      if (element) {
        element.scrollIntoView({ behavior: 'smooth' });
      }
    },
    downloadFile() {
      const url = 'Требования_к_публикации.pdf';

      const link = document.createElement('a');
      link.href = url;

      link.setAttribute('download', 'Требования_к_публикации.pdf');

      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Inter+Tight:ital,wght@0,100..900;1,100..900&display=swap');
.header {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 90px;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  background-color: transparent;
  transition: background-color 0.1s ease;
}

.sticky {
  background-color: #153A4B;
}

.container{
  max-width: 1220px;
  width: 100%;
  margin: auto;
  display: flex;
  box-sizing: border-box;
  justify-content: space-between;
  align-items: center;
}

.logo-container {
  height: 45px;
  width: auto;
}

.logo_img {
  height: 100%;
}
.nav-links ul {
  list-style: none;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.nav-links ul li {
  display: inline-block;
  margin-left: 26px;
}

.nav-links ul li button{
  background-color: transparent;
  border: none;
  color: rgba(255, 255, 255, 0.7);
  text-decoration: none;
  font-size: 18px;
  font-family: "Inter Tight", sans-serif;
}

.nav-links ul li a, router-link {
  color: rgba(255, 255, 255, 0.7);
  text-decoration: none;
  font-size: 18px;
  font-family: "Inter Tight", sans-serif;
}

.download-file-img{
  width: 24px;
  margin-right: 10px
}

.download-file-txt{
  color: #085578;
}

.download-file-btn{
  border-radius: 1000px;
  background-color: white !important;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 47px;
  width: 196px;
  padding: 10px;
}

@media (max-width: 1300px) {
  .container{
    max-width: 800px;
  }
}

@media (max-width: 450px) {
  .header{
    max-width: 430px;
  }
  .scroll_btn{
    display: none !important;
  }
  .logo-container{
    display: none;
  }
  .container{
    justify-content: center;
  }
  .nav-links ul li{
    margin: 0;
  }
}

</style>

