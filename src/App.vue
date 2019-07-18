<template>
  <div id="app">
    <div class="container-fluid">
      <b-navbar-brand href="#" class="navi">
        <img :src="logo" alt="#" class="logo" />
      </b-navbar-brand>
      <section class="contacts">
        <div class="infoGroup">
          <span class="infoCont1">+7 495 123-37-99</span>
          <div class="icons">
            <a href="https://www.instagram.com/studio_myka/"><img :src="inst" alt="#" class="inst" /></a>
            <a href="https://www.facebook.com/studiomyka/"><img :src="face" alt="#" class="face" /></a>
          </div>
          <span class="infoCont2">office@studiomyka.ru</span>
        </div>
      </section>
      <section class="textSect">
        <p
          class="text"
        >Сайт находится на реконструкции. Приглашаем прогуляться онлайн по студии! И ждем Вас!</p>
      </section>
      <iframe
        class="frame"
        src="//tour-360.ru/projects/studiomyka/"
        frameborder="no"
        scrolling="no"
        allowfullscreen
      ></iframe>
    </div>
  </div>
</template>

<script>
import logo from "./img/logoM.png";
import inst from "./img/inst.png";
import face from "./img/face.png";
import text from "./img/invalid-name.png";

export default {
  name: "app",
  components: {},
  data: () => ({
    logo: logo,
    inst: inst,
    face: face,
    text: text
  })
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Montserrat&display=swap");
@import url("https://fonts.googleapis.com/css?family=Amatic+SC&display=swap");

body {
  max-width: 100%;
}

.container-fluid {
  margin: 0;
  padding: 0;
  text-align: -webkit-center;
}

.navi {
  margin: 0;
}

#app {
  max-width: 100%;
  background-color: #000000;
  text-align: center;
}

.contacts {
  display: flex;
  justify-content: center;
}

.infoGroup {
  max-width: 100%;
  justify-content: space-between;
  display: flex;
}

.icons {
  display: flex;
  min-width: 300px;
  justify-content: space-between;
}

.infoCont1,
.infoCont2 {
  line-height: 5;
  font-family: "Montserrat", sans-serif;
  font-size: 25px;
  font-weight: normal;
  letter-spacing: normal;
  color: #ffffff;
  min-width: 400px;
}

.infoCont1:before {
  content: url(img/phone-bluetooth.png);
  padding-right: 7%;
}

.infoCont2:after {
  content: url(img/contact-mail.png);
  padding-left: 5%;
}

.frame {
  margin-top: 5%;
  margin-bottom: 3%;
}

.textSect {
  margin-top: 3%;
}

.text {
  font-family: "Amatic SC", cursive;
  font-size: 100px;
  font-weight: normal;
  font-style: normal;
  font-stretch: normal;
  line-height: normal;
  letter-spacing: normal;
  color: #ffffff;
}

.frame {
  width: 1183px;
  height: 709px;
}

@media screen and (max-width: 1160px) {
  .navi,
  .logo {
    width: 550px;
    height: 346px;
  }

  .text {
    font-size: 69px;
  }

  .infoGroup {
    flex-direction: column;
    text-align: -webkit-center;
    min-width: 100%;
  }

  .infoCont1,
  .infoCont2 {
    font-size: 17px;
    min-width: 100%;
  }

  .inst,
  .face {
    width: 100px;
    height: 100px;
  }

  .frame {
    width: 100%;
    height: 409px;
  }

  .icons {
    display: flex;
    max-width: 230px;
    min-width: 230px;
    justify-content: space-between;
  }
}

@media screen and (max-width: 715px) {
  .navi,
  .logo {
    width: 100%;
    height: 346px;
  }
}
</style>
