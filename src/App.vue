<template>
  <div>
    <header id="header">
      <img class="img_bg" src="./assets/promo/1_HEADER/1_HEADER_bg.jpg">
      <div class="header_container">
        <img src="./assets/promo/1_HEADER/1_HEADER_logo.png">
        <img src="./assets/promo/1_HEADER/1_HEADER_head.png">
        <img :src="require(`${this.btn_play_list[this.btn_play_count]}`)" v-on:mouseover="mouseover_btn" v-on:mouseout="mouseout_btn" @click="btn_add_active">
      </div>
      <div class="page_text page_text_header_widht_top">
        <p>
          Судьба планеты ангелов в твоих руках! Древнее зло вырвалось из глубины преисподней, и лишь вмешательство героя
          спасет этот мир!
          Все зависит только от твоих решений!
        </p>
      </div>
      <img class="btn_pages" src="./assets/promo/BTN_scroll_active.png" @click="go_over_page_chars">
    </header>
    <div class="chars" id="chars">
      <img class="img_bg" :src="require(`${this.chars_slider_list[this.slider_count]}`)">
      <img class="chars_h1" :src="require(`${this.chars_h1_list[this.slider_count]}`)">
      <img class="chars_slide_arrow_right" src="./assets/promo/BTN_scroll_active.png" @click="chars_slide_add_right">
      <img class="chars_slide_arrow_left" src="./assets/promo/BTN_scroll_active.png" @click="chars_slide_add_left">
      <img class="page_title" src="./assets/promo/2_CHARS/2_CHARS_head.png">
      <img class="chars_h2_img" :src="require(`${this.chars_h2_list[this.slider_count]}`)">
      <p class="chars_h2_text chars_h2_text_Isolda" v-show="chars_text_show_Isolda">Империя_бессмертных</p>
      <p class="chars_h2_text chars_h2_text_Lleyn" v-show="chars_text_show_Lleyn">Цитадель_небожителей</p>
      <p class="chars_h2_text chars_h2_text_Pamela" v-show="chars_text_show_Pamela">Союз_просвященных</p>
      <div>
        <p class="chars_h2_text chars_text_description" v-show="chars_text_show_Isolda">
          Появление королевы холода и ее верного медведя предвещает ледяная буря. Неуязвимая Изольда замораживает
          противников насмерть и не знает пощады.
        </p>
        <p class="chars_h2_text chars_text_description" v-show="chars_text_show_Lleyn">
          Зверолюд Ллейн выбрал кровавый путь наемного убийцы в тайной организации "Покров". Его прозвали “Дикий клинок”
          из-за жестокости и скорости.
        </p>
        <p class="chars_h2_text chars_text_description" v-show="chars_text_show_Pamela">
          Памела — супруга древнего огненного дракона, одна из первых овладела магией. Никто не знает, на чьей стороне
          она сражается на самом деле.
        </p>
        <div class="chars_icon_container">
          <div>
            <img :src="require(`${this.chars_icon_list1[this.slider_count]}`)" v-show="chars_icon_Isolda_show"
                 v-on:mouseover="mouseover_Isolda">
            <img src="./assets/promo/2_CHARS/2_CHARS_icon_Isolda_hover.png" v-show="chars_icon_Isolda_hover_show"
                 v-on:mouseout="mouseout_Isolda">
          </div>
          <div>
            <img :src="require(`${this.chars_icon_list2[this.slider_count]}`)" v-show="chars_icon_Lleyn_show"
                 v-on:mouseover="mouseover_Lleyn">
            <img src="./assets/promo/2_CHARS/2_CHARS_icon_Lleyn_hover.png" v-show="chars_icon_Lleyn_hover_show"
                 v-on:mouseout="mouseout_Lleyn">
          </div>
          <div>
            <img :src="require(`${this.chars_icon_list3[this.slider_count]}`)" v-show="chars_icon_Pamela_show"
                 v-on:mouseover="mouseover_Pamela">
            <img src="./assets/promo/2_CHARS/2_CHARS_icon_Pamela_hover.png" v-show="chars_icon_Pamela_hover_show"
                 v-on:mouseout="mouseout_Pamela">
          </div>
        </div>
        <div class="page_text">
          <p>
            60 наемников с неповторимой историей и сотни возможностей для построения команды ждут тебя! Система связей
            между персонажами — важная часть игрового сюжета и тонкий механизм настройки боевого отряда. Выбери свою
            фракцию и получай бонусы к мощи!
          </p>
        </div>
        <div class="chars_container_left">
          <div class="chars_container_left_img">
            <img :src="require(`${this.chars_skill_list1[this.slider_count]}`)">
          </div>
          <div class="chars_container_left_text">
            <h6 v-show="chars_text_show_Isolda">Конец зимы</h6>
            <p v-show="chars_text_show_Isolda">360% урона авангарду врага</p>
            <h6 v-show="chars_text_show_Lleyn">Дикий разрез</h6>
            <p v-show="chars_text_show_Lleyn">Превращает 30% наносимого урона в ОЗ.</p>
            <h6 v-show="chars_text_show_Pamela">Черное дыхание</h6>
            <p v-show="chars_text_show_Pamela">Наносит врагу с мин. ОЗ 426% урона</p>
          </div>
        </div>
        <div class="chars_container_left2">
          <div class="chars_container_left_img">
            <img :src="require(`${this.chars_skill_list2[this.slider_count]}`)">
          </div>
          <div class="chars_container_left_text">
            <h6 v-show="chars_text_show_Isolda">Морозная ария</h6>
            <p v-show="chars_text_show_Isolda">Ледяной щит уменьшает получаемый урон на 20%</p>
            <h6 v-show="chars_text_show_Lleyn">Найти и уничтожить</h6>
            <p v-show="chars_text_show_Lleyn">Наносит 313% урона врагу.</p>
            <h6 v-show="chars_text_show_Pamela">Проклятие дракона</h6>
            <p v-show="chars_text_show_Pamela">Проклинает всех врагов, снижая урон на 15%</p>
          </div>
        </div>
      </div>
      <img class="btn_pages" src="./assets/promo/BTN_scroll_active.png" @click="go_over_page_video">
    </div>
    <div class="video" id="video">
      <!--<img class="img_bg" src="./assets/promo/2_CHARS/2_CHARS_bg_Lleyn.jpg">-->
      <video width="100%" height="100%" autoplay muted loop>
        <source src="./assets/promo/3_VIDEO/bg.webm" type='video/webm; codecs="vp8, vorbis"'>
      </video>
      <img class="page_title" src="./assets/promo/3_VIDEO/3_VIDEO_head.png">
      <div class="page_text page_text_video_wight_top">
        <p>
          Стань самым сильным в турнирах и накажи противников с других серверов в кросс-серверных сражениях.
          Занимай места в PvP- и PvE-топах и получай эксклюзивные награды и доступ к магазинам для избранных!
        </p>
      </div>
      <img class="btn_pages" src="./assets/promo/BTN_scroll_active.png" @click="go_over_page_mount">
    </div>
    <div class="mount" id="mount">
      <img class="img_bg" src="./assets/promo/4_MOUNT/4_MOUNT_bg.jpg">
      <img class="page_title" src="./assets/promo/4_MOUNT/4_MOUNT_head.png">
      <div class="mount_container">
        <div class="mount_column_left">
          <img src="./assets/promo/4_MOUNT/4_MOUNT_rating_30000.png">
          <p>1 уровень</p>
        </div>
        <div class="mount_column_right">
          <img src="./assets/promo/4_MOUNT/4_MOUNT_rating_150000.png">
          <p>50 уровень</p>
        </div>
      </div>
      <div class="page_text page_text_mount_wight">
        <p>
          Пройди десятки элитных данжей, собери доспехи и сильнейшее оружие и приручи верных маунтов. Добывай
          ценные ресурсы для максимальной прокачки снаряжения и отряда: развивай скиллы, применяй древние кодексы
          и собирай уникальные комбинации!
          Выработай свою стратегию боя и выбери ключевые умения для победы над врагами!
        </p>
      </div>
      <img class="btn_pages" src="./assets/promo/BTN_scroll_active.png" @click="go_over_page_footer">
    </div>
    <footer>
      <img class="img_bg" src="./assets/promo/5_FOOTER/5_FOOTER_BG.jpg">
      <img class="page_title" src="./assets/promo/5_FOOTER/5_FOOTER_head.png">
      <div class="footer_container">
        <img :src="require(`${this.btn_play_list[this.btn_play_count]}`)" v-on:mouseover="mouseover_btn_footer" v-on:mouseout="mouseout_btn_footer" @click="btn_add_active_footer">
        <h6>Поделись страницей в социальной сети</h6>
        <div class="footer_social_network_container">
          <img :src="require(`${this.btn_fb_list[this.btn_fb_count]}`)" v-on:mouseover="mouseover_fb" v-on:mouseout="mouseout_fb" @click="fb_add_active">
          <img :src="require(`${this.btn_vk_list[this.btn_vk_count]}`)" v-on:mouseover="mouseover_vk" v-on:mouseout="mouseout_vk" @click="vk_add_active">
          <img :src="require(`${this.btn_ok_list[this.btn_ok_count]}`)" v-on:mouseover="mouseover_ok" v-on:mouseout="mouseout_ok" @click="ok_add_active">
          <img :src="require(`${this.btn_mail_list[this.btn_mail_count]}`)" v-on:mouseover="mouseover_mail" v-on:mouseout="mouseout_mail" @click="mail_add_active">
        </div>
        <p>Нажимая кнопку “Играть”, вы подтверждаете, что принимаете условия</p>
        <div class="footer_link_container">
          <a href="#">Пользовательского соглашения</a>
          <p>и</p>
          <a href="#">Политики приватности.</a>
        </div>
        <img src="./assets/promo/5_FOOTER/5_FOOTER_logo_101xp.png">
      </div>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      chars_slider_list: ['./assets/promo/2_CHARS/2_CHARS_bg_Isolda.jpg', './assets/promo/2_CHARS/2_CHARS_bg_Lleyn.jpg', './assets/promo/2_CHARS/2_CHARS_bg_Pamela.jpg'],
      chars_h1_list: ['./assets/promo/2_CHARS/2_CHARS_name_Isolda.png', './assets/promo/2_CHARS/2_CHARS_name_Lleyn.png', './assets/promo/2_CHARS/2_CHARS_name_Pamela.png'],
      chars_h2_list: ['./assets/promo/2_CHARS/2_CHARS_fraction_Isolda.png', './assets/promo/2_CHARS/2_CHARS_fraction_Lleyn.png', './assets/promo/2_CHARS/2_CHARS_fraction_Pamela.png'],
      img: './assets/promo/2_CHARS/2_CHARS_bg_Lleyn.jpg',
      slider_count: 0,
      chars_text_show_Isolda: true,
      chars_text_show_Lleyn: false,
      chars_text_show_Pamela: false,
      chars_icon_list1: ['./assets/promo/2_CHARS/2_CHARS_icon_Isolda_active.png', './assets/promo/2_CHARS/2_CHARS_icon_Isolda_inactive.png', './assets/promo/2_CHARS/2_CHARS_icon_Isolda_inactive.png'],
      chars_icon_list2: [ './assets/promo/2_CHARS/2_CHARS_icon_Lleyn_inactive.png', './assets/promo/2_CHARS/2_CHARS_icon_Lleyn_active.png', './assets/promo/2_CHARS/2_CHARS_icon_Lleyn_inactive.png'],
      chars_icon_list3: [ './assets/promo/2_CHARS/2_CHARS_icon_Pamela_inactive.png', './assets/promo/2_CHARS/2_CHARS_icon_Pamela_inactive.png', './assets/promo/2_CHARS/2_CHARS_icon_Pamela_active.png'],
      chars_skill_list1: ['./assets/promo/2_CHARS/2_CHARS_skill_Isolda_1.png', './assets/promo/2_CHARS/2_CHARS_skill_Lleyn_1.png', './assets/promo/2_CHARS/2_CHARS_skill_Pamela_1.png'],
      chars_skill_list2: ['./assets/promo/2_CHARS/2_CHARS_skill_Isolda_2.png', './assets/promo/2_CHARS/2_CHARS_skill_Lleyn_2.png', './assets/promo/2_CHARS/2_CHARS_skill_Pamela_2.png'],
      btn_play_count: 0,
      btn_play_list: ['./assets/promo/BTN_play_normal.png', './assets/promo/BTN_play_hover.png', './assets/promo/BTN_play_active.png'],
      btn_fb_count: 0,
      btn_fb_list: ['./assets/promo/5_FOOTER/5_FOOTER_btn_fb_normal.png', './assets/promo/5_FOOTER/5_FOOTER_btn_fb_hover.png', './assets/promo/5_FOOTER/5_FOOTER_btn_fb_active.png'],
      btn_vk_count: 0,
      btn_vk_list: ['./assets/promo/5_FOOTER/5_FOOTER_btn_vk_normal.png', './assets/promo/5_FOOTER/5_FOOTER_btn_vk_hover.png', './assets/promo/5_FOOTER/5_FOOTER_btn_vk_active.png'],
      btn_ok_count: 0,
      btn_ok_list: ['./assets/promo/5_FOOTER/5_FOOTER_btn_ok_normal.png', './assets/promo/5_FOOTER/5_FOOTER_btn_ok_hover.png', './assets/promo/5_FOOTER/5_FOOTER_btn_ok_active.png'],
      btn_mail_count: 0,
      btn_mail_list: ['./assets/promo/5_FOOTER/5_FOOTER_btn_mail_normal.png', './assets/promo/5_FOOTER/5_FOOTER_btn_mail_hover.png', './assets/promo/5_FOOTER/5_FOOTER_btn_mail_active.png'],
      chars_icon_Isolda_show: true,
      chars_icon_Isolda_hover_show: false,
      chars_icon_Lleyn_show: true,
      chars_icon_Lleyn_hover_show: false,
      chars_icon_Pamela_show: true,
      chars_icon_Pamela_hover_show: false,
      pages_count: 0,
      header_show: true,
      chars_show: true,
      video_show: true,
      mount_show: true,
      footer_show: true,
      btn_normal_show: true,
      btn_hover_show: false,
      btn_active_show: false,
      btn_footer_normal_show: true,
      btn_footer_hover_show: false,
      btn_footer_active_show: false,
      fb_normal_show: true,
      fb_hover_show: false,
      fb_active_show: false,
      vk_normal_show: true,
      vk_hover_show: false,
      vk_active_show: false,
      ok_normal_show: true,
      ok_hover_show: false,
      ok_active_show: false,
      mail_normal_show: true,
      mail_hover_show: false,
      mail_active_show: false
    }
  },
  methods: {
    chars_slide_add_right() {
      this.slider_count++
      if (this.slider_count > 2) {
        this.slider_count = 0
      }
      if (this.slider_count === 0) {
        this.chars_text_show_Isolda = true
        this.chars_text_show_Lleyn = false
        this.chars_text_show_Pamela = false
      }
      if (this.slider_count === 1) {
        this.chars_text_show_Isolda = false
        this.chars_text_show_Lleyn = true
        this.chars_text_show_Pamela = false
      }
      if (this.slider_count === 2) {
        this.chars_text_show_Isolda = false
        this.chars_text_show_Lleyn = false
        this.chars_text_show_Pamela = true
      }
    },
    chars_slide_add_left() {
      this.slider_count--
      if (this.slider_count < 0) {
        this.slider_count = 2
      }
      if (this.slider_count === 0) {
        this.chars_text_show_Isolda = true
        this.chars_text_show_Lleyn = false
        this.chars_text_show_Pamela = false
      }
      if (this.slider_count === 1) {
        this.chars_text_show_Isolda = false
        this.chars_text_show_Lleyn = true
        this.chars_text_show_Pamela = false
      }
      if (this.slider_count === 2) {
        this.chars_text_show_Isolda = false
        this.chars_text_show_Lleyn = false
        this.chars_text_show_Pamela = true
      }
    },
    go_over_page_chars() {
      let header_height = document.getElementById('header').scrollHeight
      window.scroll(0, header_height)
    },
    go_over_page_video() {
      let header_height = document.getElementById('header').scrollHeight
      let chars_height = document.getElementById('chars').scrollHeight
      window.scroll(0, header_height + chars_height)
    },
    go_over_page_mount() {
      let header_height = document.getElementById('header').scrollHeight
      let chars_height = document.getElementById('chars').scrollHeight
      let video_height = document.getElementById('video').scrollHeight
      window.scroll(0, header_height + chars_height + video_height)
    },
    go_over_page_footer() {
      let header_height = document.getElementById('header').scrollHeight
      let chars_height = document.getElementById('chars').scrollHeight
      let video_height = document.getElementById('video').scrollHeight
      let mount_height = document.getElementById('mount').scrollHeight
      window.scroll(0, header_height + chars_height + video_height + mount_height)
    },
    mouseover_Lleyn() {
      if (this.slider_count === 0 || this.slider_count === 2) {
        this.chars_icon_Lleyn_show = false
        this.chars_icon_Lleyn_hover_show = true
      }
    },
    mouseout_Lleyn() {
      if (this.slider_count === 0 || this.slider_count === 2) {
        this.chars_icon_Lleyn_show = true
        this.chars_icon_Lleyn_hover_show = false
      }
    },
    mouseover_Isolda() {
      if (this.slider_count === 1 || this.slider_count === 2) {
        this.chars_icon_Isolda_show = false
        this.chars_icon_Isolda_hover_show = true
      }
    },
    mouseout_Isolda() {
      if (this.slider_count === 1 || this.slider_count === 2) {
        this.chars_icon_Isolda_show = true
        this.chars_icon_Isolda_hover_show = false
      }
    },
    mouseover_Pamela() {
      if (this.slider_count === 0 || this.slider_count === 1) {
        this.chars_icon_Pamela_show = false
        this.chars_icon_Pamela_hover_show = true
      }
    },
    mouseout_Pamela() {
      if (this.slider_count === 0 || this.slider_count === 1) {
        this.chars_icon_Pamela_show = true
        this.chars_icon_Pamela_hover_show = false
      }
    },
    mouseover_fb() {
      this.btn_fb_count = 1
    },
    mouseout_fb() {
      this.btn_fb_count = 0
    },
    fb_add_active() {
      this.btn_fb_count = 2
    },
    mouseover_vk() {
      this.btn_vk_count = 1
    },
    mouseout_vk() {
      this.btn_vk_count = 0
    },
    vk_add_active() {
      this.btn_vk_count = 2
    },
    mouseover_ok() {
      this.btn_ok_count = 1
    },
    mouseout_ok() {
      this.btn_ok_count = 0
    },
    ok_add_active() {
      this.btn_ok_count = 2
    },

    mouseover_mail() {
      this.btn_mail_count = 1
    },
    mouseout_mail() {
      this.btn_mail_count = 0
    },
    mail_add_active() {
      this.btn_mail_count = 2
    },
    mouseover_btn() {
      this.btn_play_count = 1
    },
    mouseout_btn () {
      this.btn_play_count = 0
    },
    btn_add_active () {
      this.btn_play_count = 2
    },
    mouseover_btn_footer() {
      this.btn_play_count = 1
    },
    mouseout_btn_footer () {
      this.btn_play_count = 0
    },
    btn_add_active_footer () {
      this.btn_play_count = 2
    }
  }
}
</script>

<style>
/*All styles*/
body, p, a {
  margin: 0;
  padding: 0;
}

header, .chars, .video, .img_bg, .mount, footer {
  width: 100vw;
  height: 100vh;
  position: relative;
}

.btn_pages {
  width: 4.6%;
  overflow: auto;
  margin: auto;
  position: absolute;
  top: 90%;
  left: 0;
  bottom: 0;
  right: 0;
  z-index: 100;
}

.page_title {
  width: 45%;
  overflow: auto;
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 80%;
  right: 0;
  transform: none;
  z-index: 100;
}

.page_text {
  position: absolute;
  overflow: auto;
  /*width: 1000px;*/
  width: 55%;
  margin: auto;
  top: 74%;
  left: 0;
  bottom: 0;
  right: 0;
  text-align: center;
  z-index: 100;
}

.page_text p {
  font-size: 24px;
  color: rgb(249, 244, 233);
  line-height: 1.5;
  text-align: center;
  height: 95px;
}

/*Style for HEADER*/
.header_container {
  width: 68%;
  overflow: auto;
  margin: auto;
  position: absolute;
  top: 3%;
  left: 0;
  bottom: 0;
  right: 0;
  text-align: center;
}

.page_text_header_widht_top {
  top: 80%;
  /*width: 800px;*/
  width: 45%;
}

/*Style for CHARS*/

.chars_slide_arrow_right, .chars_slide_arrow_left, .chars_head, .chars_h1, .chars_h2_img, .chars_h2_text {
  position: absolute;
  transform: rotate(270deg);
  right: 5%;
  top: 40%;
  z-index: 100;
}

.chars_slide_arrow_left {
  left: 5%;
  transform: rotate(90deg);
}

.chars_h1 {
  left: 17%;
  top: 10%;
  transform: none;
}

.chars_h2_img, .chars_h2_text {
  left: 19.3%;
  top: 24%;
  transform: none;
}

.chars_h2_text {
  left: 21.5%;
  top: 22.5%;
  font-size: 21px;
  line-height: 1.333;
  text-shadow: 0px 5px 30px rgba(35, 27, 32, 0.004);
  /*width: 293px;*/
  width: 17.3%;
}

.chars_h2_text_Isolda {
  color: rgb(255, 50, 58);
  margin-top: 18px;
}

.chars_h2_text_Lleyn {
  color: rgb(255, 196, 25);
  margin-top: 18px;
}

.chars_h2_text_Pamela {
  color: rgb(202, 134, 255);
  margin-top: 18px;
}

.chars_text_description {
  font-size: 24px;
  color: rgb(249, 244, 233);
  line-height: 1.5;
  text-align: left;
  text-shadow: 0px 5px 30px rgba(35, 27, 32, 0.004);
  left: 19.3%;
  top: 29%;
  /*width: 400px;*/
  width: 19.4%;
}

.chars_icon_container {
  position: absolute;
  z-index: 100;
  right: 18.5%;
  top: 16%;
}

.chars_icon_container img {
  margin-bottom: 70px;
}

.chars_container_left, .chars_container_left2 {
  position: absolute;
  display: flex;
  z-index: 100;
  top: 50%;
  left: 19.5%;
}

.chars_container_left2 {
  top: 58%;
}

.chars_container_left_text {
  margin-left: 17px;
}

.chars_container_left_text h6 {
  margin: 0;
  font-size: 24px;
  color: rgb(249, 244, 233);

}

.chars_container_left_text p {
  margin: 0;
  font-size: 16px;
  color: rgb(188, 190, 193);
  line-height: 2.25;
}

/*Style for VIDEO*/
.video {
  background: black;
}

/*Style for MOUNT*/
.mount_container {
  width: 68%;
  overflow: auto;
  margin: auto;
  position: absolute;
  top: 58%;
  left: 0;
  bottom: 0;
  right: 0;
  display: flex;
  justify-content: space-between;
}

.page_text_mount_wight {
  width: 1000px;
}

.mount_column_left, .mount_column_right {
  text-align: center;
}

.mount_column_left p, .mount_column_right p {
  margin: 0;
  font-size: 24px;
  color: rgb(255, 196, 25);
  line-height: 1.167;
  text-shadow: 0px 5px 30px rgba(35, 27, 32, 0.004);
  margin-top: -30px;
}

/*Style for FOOTER*/
.footer_container {
  position: absolute;
  text-align: center;
  width: 50%;
  overflow: auto;
  margin: auto;
  position: absolute;
  top: 15%;
  left: 0;
  bottom: 0;
  right: 0;
}

.footer_container img {
  margin-top: 50px;
}

.footer_container h6 {
  margin: 0;
  margin-top: 65px;
  font-size: 24px;
  color: rgb(249, 244, 233);
  line-height: 1.125;
}

.footer_social_network_container {
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  width: 36%;
}

.footer_container p {
  font-size: 14px;
  color: rgba(181, 181, 181, 0.502);
  line-height: 1.489;
  margin-top: 90px;
}

.footer_link_container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 34%;
  margin: 0 auto;
}

.footer_link_container a, .footer_link_container p {
  font-size: 14px;
  color: rgba(211, 211, 211, 0.502);
  text-decoration: underline;
  line-height: 1.489;
  margin: 0;
}

.page_text_video_wight_top {
  top: 80%;
  /*width: 1100px;*/
  width: 55%;
}
</style>
