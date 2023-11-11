<script lang="ts" setup>
import {ref} from "vue";

const show = ref(false);
const show2 = ref(false);
const show3 = ref(false);
const show4 = ref(false);
const show5 = ref(false);

const extension = ref(false)
const burger = ref(false)

const burger__extension = ref(false)
</script>

<template>
  <header class="header">
    <div class="">
      <div class="container">
        <div class="navbar relative">
          <div class="grid align-items-center">
            <div class="col">
              <div class="flex align-items-center justify-content-between">
                <router-link to="/">
                  <img
                      class=" h59px"
                      src="https://s3-alpha-sig.figma.com/img/8180/d86f/80686ec215071f4ca9f5d162f3803549?Expires=1698624000&Signature=Rn6oBadFxGGATI8fGNVWHvs~mcYWCdWM9lkjmHCF~465bTRMksBGg0Eg80Fc1RbW~i4~AdH6b9ISC6Yj80byy0AbtEIYnh3LxVb6r5vzgpbqo371JUJk3QS6rqInVvTsOtYi2a1yAGsvGl6Vh-~FVjEPf~viyIe43-nZ-aC48PsQ6Vi1xH-kJ59AEePqMj5Ts0Eyvxqgcxc8Ad9J5BJdxRgkU84t9-PR08Eq37GK9APuckzuZvLEp2Vl0PrJUatjZsxL6WXWvc4h9YkzZc1IAJA7BXsndB4LM~BEjqvLlTGvGUraOaCjAEJmhOSE0WBakc4FRXXK5FKCPhC6qtgJiA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                      alt="">
                </router-link>
                <span>
                  <p class="header__menu__text">
                    <p class="header__menu__text  text-white"
                       v-if="extension==false" @click="extension=true">услуги</p>
                    <p class="header__menu__text relative  text-white" v-if="extension"
                       @click="extension=false">услуги</p>
                  </p>
                </span>
                <span>
                  <p class="header__menu__text">
                    <router-link to="portfolio" class="header__menu__text text-white">портфолио</router-link>
                  </p>
                </span>
                <span>
                  <p class="header__menu__text">
                    <router-link to="about__us" class="header__menu__text text-white">о нас</router-link>
                  </p>
                </span>
                <span>
                <p class="header__menu__text">
                  <a href="#contacts" class="header__menu__text text-white">контакты</a>
                </p>
              </span>
              </div>
            </div>
            <a href="" class="header__tel ">+7 (343) 364-28-75</a>
            <div class="col ">
              <div class="flex justify-content-end align-items-end">
                <img src="public/logo-instagram%202.png" class="pr-5 object-cover h30px header__instalogo" alt="">
                <img src="public/menu.png" alt="" v-if="burger==false" @click="burger=true"
                     class="h20px header__icon pr-2">
                <img src="public/menu.png" alt="" v-if="burger==true" @click="burger=false"
                     class="h20px header__icon pr-2">
                <div class="outer-container">
                  <Button label="связаться" class="w130px h-40px border-noround bg-gray border-none alfa"
                          severity="secondary" raised/>
                </div>
              </div>
            </div>
          </div>
          <div class="dropdown__item " v-if="extension">
            <p class="dropdown__items">
              <router-link class="dropdown__items" to="interior__design">ДИЗАЙН ИНТЕРЬЕРА</router-link>
            </p>
            <p class="dropdown__items">
              <router-link class="dropdown__items" to="repair__areas">РЕМОНТНЫЕ РАБОТЫ</router-link>
            </p>
            <p class="dropdown__items">
              <router-link class="dropdown__items" to="construction__cottages">СТРОИТЕЛЬСТВО КОТТЕДЖЕЙ</router-link>
            </p>
            <p class="dropdown__items">
              <router-link class="dropdown__items" to="project__completion">КОМПЛЕКТАЦИЯ ПРОЕКТОВ</router-link>
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="pl-4 pt-4" v-if="burger">
        <p class="extra__text  text-white" v-if="burger__extension==false" @click="burger__extension=true">услуги</p>
        <p class="extra__text   text-white" v-if="burger__extension" @click="burger__extension=false">услуги</p>
        <div class="">
          <div class="burger__extension mt-3 mb-3" v-if="burger__extension">
            <p class="">
              <router-link to="interior__design" class="dropdown__items">ДИЗАЙН ИНТЕРЬЕРА</router-link>
            </p>
            <p class="">
              <router-link to="repair__areas" class="dropdown__items">РЕМОНТНЫЕ РАБОТЫ</router-link>
            </p>
            <p class="">
              <router-link to="construction__cottages" class="dropdown__items">СТРОИТЕЛЬСТВО КОТТЕДЖЕЙ</router-link>
            </p>
            <p class="">
              <router-link to="project__completion" class="dropdown__items">КОМПЛЕКТАЦИЯ ПРОЕКТОВ</router-link>
            </p>

          </div>
        </div>
        <p>
          <router-link to="portfolio" class="extra__text pt-2">портфолио</router-link>
        </p>
        <p>
          <router-link to="about__us" class="extra__text pt-2 ">о нас</router-link>
        </p>
        <p>
          <a href="#contacts" class="extra__text pt-2 ">контакты</a>
        </p>
        <div class="flex pt-3">
          <img src="public/logo-instagram%202.png" class="pr-5 object-cover h30px " alt="">
          <Button label="связаться" class="w130px h-40px border-noround bg-gray border-none alfa"
                  severity="secondary" raised/>
        </div>
      </div>
    </div>
  </header>
  <div class="banner">
    <div class="container">
      <div class="grid">
        <div class="col-12 md:col-7">
          <img src="http://dom-uyta.ru/img/des.png" class="w-full h-full object-cover" alt="">
        </div>
        <div class="col-12 md:col-5">

          <h1 class="banner__title text-right	text-white"> Уникальный <br>
            дизайн интерьера</h1>
          <div class="flex justify-content-end">
            <ul class="">
              <li class="banner__text li pl-3 pt-2">разработаем дизайн-проект</li>
              <li class="banner__text li pl-3 pt-2">выполним отделочные работы под ключ</li>
              <li class="banner__text li pl-3 pt-2">укомплектуем материалами и мебелью</li>
              <li class="banner__text li pl-3 pt-2">от проекта до полной реализации – один подрядчик</li>
            </ul>
          </div>
          <div class="flex justify-content-end">
            <Button label="связаться" severity="secondary" class="btn__text pt-3 pb-3 pl-3 mt-7 "/>
          </div>
        </div>
      </div>
    </div>
  </div>
  <div class="banner02">
    <div class="container">
      <h1 class="banner__title text-right	text-white pt-4"> Уникальный <br>
        дизайн интерьера</h1>
      <div class="flex justify-content-end">
        <ul class="pb-4">
          <li class="banner__text li pl-3 pt-2">разработаем дизайн-проект</li>
          <li class="banner__text li pl-3 pt-2">выполним отделочные работы под ключ</li>
          <li class="banner__text li pl-3 pt-2">укомплектуем материалами и мебелью</li>
          <li class="banner__text li pl-3 pt-2">от проекта до полной реализации – один подрядчик</li>
        </ul>
      </div>
      <div class="flex justify-content-end">
        <Button label="связаться" severity="secondary" class="btn__text pt-3 pb-3 pl-3 mt-4 mb-5 "/>
      </div>
    </div>
  </div>
  <section class="design__project">
    <div class="service-content ">
      <div class="container ">
        <div class="grid pt-3 ">
          <div class="col-12">
            <p class="custom-title">
              С дизайн-проектом вы получите:
            </p>
          </div>
        </div>
        <div class="grid">
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="71" height="62" viewBox="0 0 71 62" fill="none" xmlns="http://www.w3.org/2000/svg">
                <mask id="path-1-outside-1" maskUnits="userSpaceOnUse" x="0" y="0.759766" width="71" height="61"
                      fill="black">
                  <rect fill="white" y="0.759766" width="71" height="61"/>
                  <path d="M36.5952 43.323V58.4617H38.7857V43.323H36.5952Z"/>
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M69.009 60.3746H1.99101C1.72818 60.3746 1.47611 60.2739 1.29026 60.0947C1.10441 59.9155 1 59.6724 1 59.419V2.71542C1 2.46196 1.10441 2.21889 1.29026 2.03967C1.47611 1.86045 1.72818 1.75977 1.99101 1.75977H62.1375C62.4003 1.75977 62.6524 1.86045 62.8382 2.03967C63.0241 2.21889 63.1285 2.46196 63.1285 2.71542V30.9882H69.0081C69.2707 30.988 69.5226 31.0882 69.7085 31.2669C69.8945 31.4456 69.9993 31.6882 70 31.9413V59.419C70 59.6724 69.8956 59.9155 69.7097 60.0947C69.5239 60.2739 69.2718 60.3746 69.009 60.3746ZM17.0606 58.4617V53.9371H9.19375C8.93092 53.9371 8.67885 53.8364 8.493 53.6572C8.30715 53.478 8.20274 53.2349 8.20274 52.9814V36.347H2.98375L2.98289 58.4617H17.0606ZM2.98289 34.4332H8.20446H10.1865V52.025H18.0516C18.3145 52.025 18.5665 52.1256 18.7524 52.3049C18.9382 52.4841 19.0426 52.7272 19.0426 52.9806L19.0435 58.4617H38.7857H68.0163V32.9011H43.8176C43.5548 32.9011 43.3027 32.8005 43.1169 32.6212C42.931 32.442 42.8266 32.199 42.8266 31.9455V30.1007H40.378V28.1878H42.8258V22.0056H44.8095V30.9882H51.1992H53.1813H54.0095H55.7345H61.1456V3.6719H55.7345H54.0095H53.1813H51.1992H48.5065V12.417H46.5228V9.48852H30.94C30.6771 9.48852 30.4251 9.38783 30.2392 9.20861C30.0534 9.02939 29.9489 8.78632 29.9489 8.53287V3.6719H26.3265H24.3427H23.2732H21.286H16.5975H14.6154H11.0128H9.02988H2.98375V15.3776V17.2897V22.325V24.5698L2.98289 34.4332ZM31.931 7.57638H46.5236V3.6719H31.931V7.57638Z"/>
                  <path
                      d="M11.0128 16.3341V3.6719H9.02988V15.3776H7.74216H2.98375V17.2897H6.75029H8.73317H10.0218C10.2846 17.2897 10.5367 17.189 10.7225 17.0098C10.9084 16.8306 11.0128 16.5875 11.0128 16.3341Z"/>
                  <path
                      d="M24.3444 18.2495V22.6576L2.98375 22.325V24.5698H8.20446H10.1865H24.3453V34.7858H26.329V30.1016H28.7725V28.1886H26.3282V18.2495H24.3444Z"/>
                  <path d="M55.7345 30.9882V3.6719H54.0095V30.9882H55.7345Z"/>
                </mask>
                <path d="M36.5952 43.323V58.4617H38.7857V43.323H36.5952Z" fill="white"/>
                <path fill-rule="evenodd" clip-rule="evenodd"
                      d="M69.009 60.3746H1.99101C1.72818 60.3746 1.47611 60.2739 1.29026 60.0947C1.10441 59.9155 1 59.6724 1 59.419V2.71542C1 2.46196 1.10441 2.21889 1.29026 2.03967C1.47611 1.86045 1.72818 1.75977 1.99101 1.75977H62.1375C62.4003 1.75977 62.6524 1.86045 62.8382 2.03967C63.0241 2.21889 63.1285 2.46196 63.1285 2.71542V30.9882H69.0081C69.2707 30.988 69.5226 31.0882 69.7085 31.2669C69.8945 31.4456 69.9993 31.6882 70 31.9413V59.419C70 59.6724 69.8956 59.9155 69.7097 60.0947C69.5239 60.2739 69.2718 60.3746 69.009 60.3746ZM17.0606 58.4617V53.9371H9.19375C8.93092 53.9371 8.67885 53.8364 8.493 53.6572C8.30715 53.478 8.20274 53.2349 8.20274 52.9814V36.347H2.98375L2.98289 58.4617H17.0606ZM2.98289 34.4332H8.20446H10.1865V52.025H18.0516C18.3145 52.025 18.5665 52.1256 18.7524 52.3049C18.9382 52.4841 19.0426 52.7272 19.0426 52.9806L19.0435 58.4617H38.7857H68.0163V32.9011H43.8176C43.5548 32.9011 43.3027 32.8005 43.1169 32.6212C42.931 32.442 42.8266 32.199 42.8266 31.9455V30.1007H40.378V28.1878H42.8258V22.0056H44.8095V30.9882H51.1992H53.1813H54.0095H55.7345H61.1456V3.6719H55.7345H54.0095H53.1813H51.1992H48.5065V12.417H46.5228V9.48852H30.94C30.6771 9.48852 30.4251 9.38783 30.2392 9.20861C30.0534 9.02939 29.9489 8.78632 29.9489 8.53287V3.6719H26.3265H24.3427H23.2732H21.286H16.5975H14.6154H11.0128H9.02988H2.98375V15.3776V17.2897V22.325V24.5698L2.98289 34.4332ZM31.931 7.57638H46.5236V3.6719H31.931V7.57638Z"
                      fill="white"/>
                <path
                    d="M11.0128 16.3341V3.6719H9.02988V15.3776H7.74216H2.98375V17.2897H6.75029H8.73317H10.0218C10.2846 17.2897 10.5367 17.189 10.7225 17.0098C10.9084 16.8306 11.0128 16.5875 11.0128 16.3341Z"
                    fill="white"/>
                <path
                    d="M24.3444 18.2495V22.6576L2.98375 22.325V24.5698H8.20446H10.1865H24.3453V34.7858H26.329V30.1016H28.7725V28.1886H26.3282V18.2495H24.3444Z"
                    fill="white"/>
                <path d="M55.7345 30.9882V3.6719H54.0095V30.9882H55.7345Z" fill="white"/>

              </svg>
            </div>
            <p class="custom-text">
              Планировку <br>
              и рабочие чертежы
            </p>
          </div>
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="68" height="68" viewBox="0 0 68 68" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M65.3436 10.4513H52.3278V6.98782C52.3278 6.28329 52.0482 5.60782 51.5501 5.10925C44.7379 -1.70256 33.7108 -1.7036 26.8975 5.10925C26.3995 5.60782 26.1198 6.28329 26.1198 6.98782V10.4513H15.7604V2.66001C15.7604 1.19336 14.5712 0.00428009 13.104 0.00428009C5.87882 0.00428009 0 5.88226 0 13.1076V54.8967C0 62.122 5.87882 68 13.104 68H65.3436C66.8109 68 68 66.8109 68 65.3443V13.1076C67.9995 11.6404 66.8103 10.4513 65.3436 10.4513ZM31.4321 8.15148C35.9251 4.36789 42.5235 4.36893 47.0155 8.15148V39.3032C42.1261 36.8654 36.3215 36.8654 31.4321 39.3032V8.15148ZM45.705 44.6593L39.2238 51.1401L32.7421 44.6593C36.6847 42.1628 41.7629 42.1628 45.705 44.6593ZM5.31226 13.1076C5.31226 9.74367 7.45502 6.87109 10.4481 5.78265V42.0637C8.55597 42.4549 6.81167 43.2549 5.31226 44.3672V13.1076ZM62.6872 62.688H13.104C8.8076 62.688 5.31226 59.1929 5.31226 54.8967C5.31226 50.6006 8.8076 47.1054 13.104 47.1054C14.5712 47.1054 15.7604 45.9163 15.7604 44.4492V15.7633H26.1198C26.2158 46.0502 25.7328 45.1625 26.8975 46.3272L37.3451 56.7748C38.3817 57.8113 40.0648 57.8118 41.102 56.7748C52.2152 45.6554 51.6554 46.2619 51.8827 45.921C52.6967 44.7013 52.1805 45.3374 52.3278 15.7633H62.6872V62.688Z"
                    fill="white"/>
              </svg>

            </div>
            <p class="custom-text">
              Ведомость <br>
              материалов
            </p>
          </div>
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="68" height="68" viewBox="0 0 68 68" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path fill-rule="evenodd" clip-rule="evenodd"
                      d="M65.7333 68H2.26667C1.01396 68 0 67.048 0 65.8736V55.2514V50.9986V2.125C0 0.950583 1.01396 0 2.26667 0H31.7318H36.2667H65.7333C66.9845 0 68 0.950583 68 2.125V50.9986V55.2514V65.8736C68 67.048 66.9845 68 65.7333 68ZM31.7313 4.24731H6.79951C5.5468 4.24731 4.53284 5.20073 4.53284 6.37656V50.9987H31.7313V4.24731ZM63.4664 6.37656C63.4664 5.20073 62.451 4.24731 61.1998 4.24731H36.2664V50.9987H63.4664V6.37656ZM63.4662 55.2512H36.2662H31.7313H4.53284V61.6234C4.53284 62.8006 5.5468 63.7498 6.79951 63.7498H61.1995C62.4507 63.7498 63.4662 62.8006 63.4662 61.6234V55.2512ZM45.3323 38.25H40.8005V25.5H45.3323V38.25ZM27.2 38.25H22.6667V25.5H27.2V38.25Z"
                      fill="white"/>
              </svg>

            </div>
            <p class="custom-text">
              Эксклюзивный дизайн <br>
              c 3D визуализацией
            </p>
          </div>
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="48" height="59" viewBox="0 0 48 59" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M28.715 37.5071H16.5664V43.1543H36.531V49.7286H16.5664V59H6.79646V49.7286H0V43.1543H6.79646V37.5071H0V28.8257H6.79646V0H28.715C34.0956 0 38.6549 1.85429 42.3929 5.56286C46.131 9.15905 48 13.6262 48 18.9643C48 24.19 46.131 28.601 42.3929 32.1971C38.6549 35.7371 34.0956 37.5071 28.715 37.5071ZM28.715 9.10286H16.5664V28.8257H28.715C31.4336 28.8257 33.6708 27.8705 35.4265 25.96C37.2956 24.0495 38.2301 21.7176 38.2301 18.9643C38.2301 16.211 37.2956 13.879 35.4265 11.9686C33.6708 10.0581 31.4336 9.10286 28.715 9.10286Z"
                    fill="white"/>
              </svg>

            </div>
            <p class="custom-text">
              Сметную стоимость <br>
              отделочных работ
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="content1 pt-7">
    <div class="container pb-7">
      <div class="grid pb-5">
        <div class="col-12 md:col-6 ">
          <img src="http://dom-uyta.ru/img/img06_n.png" alt="" class="w-full  ">
        </div>
        <div class="col-12 md:col-6 pl-3">
          <div class="desc">
            <p class="custom-title pt-3 ">Комплектуем проекты</p>
            <p class="pb-3 custom-text">
              В нашем салоне, мы с Вами сможем выбрать разные отделочные материалы. Мы подготовим план-график поставки в
              соответствии с которым закупим и доставим вам все необходимые материалы по вашему проекту.
            </p>
            <div class="grid">
              <div class="col">
                <svg width="62" height="61" viewBox="0 0 62 61" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M60.5 1.98355C60.5 2.52641 60.0598 2.96664 59.5165 2.96664H52.6335V18.7002H58.5334C59.6191 18.7011 60.4986 19.5811 60.5 20.6668V58.0334C60.4986 59.1191 59.6191 59.9986 58.5334 60H5.43327C4.34755 59.9986 3.46799 59.1191 3.46664 58.0334V50.1668H2.48354C1.94023 50.1668 1.5 49.7266 1.5 49.1833C1.5 48.6404 1.94023 48.2002 2.48354 48.2002H8.38345V25.5125L4.43938 29.0749C3.82089 29.6348 3.46754 30.4298 3.46664 31.2643V34.4333C3.46664 34.9766 3.02641 35.4168 2.48354 35.4168C1.94023 35.4168 1.5 34.9766 1.5 34.4333V31.2643C1.5009 29.8734 2.09013 28.5478 3.12183 27.6151L31.4659 2.0146C32.1879 1.36101 33.1278 0.999101 34.1019 1H59.5165C60.0598 1 60.5 1.44023 60.5 1.98355ZM40.8332 2.96664H34.1019C33.6148 2.96619 33.1453 3.14669 32.7843 3.47349L31.9835 4.19686V28.5334H34.9333C35.4761 28.5329 35.9164 28.0927 35.9168 27.5498V20.6668H34.9333C34.3904 20.6668 33.9502 20.2266 33.9502 19.6833C33.9502 19.1404 34.3904 18.7002 34.9333 18.7002H40.8332V2.96664ZM24.1165 28.5334H26.0832H30.0165V5.97354L21.1668 13.9666V38.3665H24.1165C24.6594 38.3661 25.0996 37.9263 25.1001 37.3835V30.5H24.1165C23.5737 30.5 23.1335 30.0598 23.1335 29.5165C23.1335 28.9736 23.5737 28.5334 24.1165 28.5334ZM19.2002 15.7432L10.3501 23.7363V48.2002H13.2998C13.8427 48.1997 14.2829 47.7595 14.2834 47.2166V40.3332H13.2998C12.757 40.3332 12.3167 39.893 12.3167 39.3501C12.3167 38.8068 12.757 38.3665 13.2998 38.3665H19.2002V15.7432ZM42.7998 18.7002H50.6668V2.96664H42.7998V18.7002ZM50.1195 58.0334H58.5334V20.6655H51.6549L51.6499 20.6668L51.6454 20.6659L41.8181 20.6668H37.8835V27.5498C37.8817 29.1784 36.5619 30.4982 34.9333 30.5H27.0667V37.3835C27.0649 39.012 25.7451 40.3314 24.1165 40.3332H16.25V47.2166C16.2482 48.8452 14.9284 50.165 13.2998 50.1668H5.43327V58.0334H37.4468H50.1195Z"
                        fill="white" stroke="white" stroke-width="2"/>
                </svg>
                <p class="pt-2 custom-text">Авторский надзор</p>
              </div>
              <div class="col">
                <svg width="58" height="57" viewBox="0 0 58 57" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path
                      d="M56.885 18.4735C55.696 15.446 53.5158 11.0779 49.8808 7.46018C46.2588 3.85495 41.9369 1.73705 38.9491 0.595048C35.669 -0.658613 31.9416 0.131591 29.4534 2.60808L20.71 11.3106C18.1182 13.8901 17.3712 17.8594 18.851 21.1876C19.3099 22.2198 19.809 23.2294 20.3423 24.2049L1.15216 43.3949C0.734567 43.8125 0.5 44.3788 0.5 44.9694V54.7662C0.5 55.9959 1.49683 56.9928 2.72655 56.9928H12.5234C13.7531 56.9928 14.7499 55.9959 14.7499 54.7662V50.7584L18.7577 50.7583C19.9875 50.7583 20.9843 49.7615 20.9843 48.5317V44.5241H24.9921C26.2218 44.5241 27.2186 43.5272 27.2186 42.2975C27.2186 41.0678 26.2218 40.071 24.9921 40.071H18.7577C17.528 40.071 16.5312 41.0678 16.5312 42.2975V46.3052L12.5234 46.3053C11.2937 46.3053 10.2968 47.3021 10.2968 48.5319V52.5397H4.95311V45.8916L24.6976 26.1472C25.423 25.4218 25.559 24.2948 25.0269 23.4178C24.2553 22.146 23.5465 20.7869 22.9203 19.3783C22.1856 17.726 22.5599 15.7523 23.8517 14.4666L32.595 5.76422C33.8433 4.52191 35.7134 4.12569 37.3596 4.7547C39.9448 5.74284 43.6708 7.56171 46.7396 10.6163C49.8273 13.6894 51.7071 17.4704 52.7402 20.1011C53.3849 21.743 52.9931 23.6083 51.7421 24.8534L42.8931 33.6609C41.6045 34.9433 39.6812 35.3183 37.9929 34.6161C36.6006 34.037 35.252 33.349 33.9851 32.5714C32.9372 31.9281 31.5661 32.2563 30.9229 33.3043C30.2796 34.3524 30.6077 35.7235 31.6557 36.3667C33.1199 37.2654 34.6767 38.0597 36.2827 38.7277C39.6384 40.1236 43.4661 39.3734 46.0345 36.8172L54.8835 28.0097C57.3933 25.5116 58.179 21.7685 56.885 18.4735Z"
                      fill="white"/>
                </svg>
                <p class="pt-2 custom-text">Ремонт “под ключ”</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="service-promo">
    <div class="container pb-7">
      <div class="grid">
        <div class="col-12 text-center">

          <div class="icon pt-5 pb-5">
            <svg width="79" height="49" viewBox="0 0 79 49" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path fill-rule="evenodd" clip-rule="evenodd"
                    d="M32.6852 0.75H48.7686L16.6019 49H0.518555L32.6852 0.75ZM62.611 0.75H78.6944L46.5277 49H30.4444L62.611 0.75Z"
                    fill="#E1A600"/>
            </svg>
          </div>
          <p class="custom-title text-center pb-5">Качественный дизайн-проект поможет Вам:</p>
        </div>
        <div class="clearfix"></div>
        <div class="col-12 md:col-4">
          <div class="flex align-items-center">
            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                  d="M8 1C11.866 1 15 4.13401 15 8C15 11.866 11.866 15 8 15C4.13401 15 1 11.866 1 8C0.999999 4.13401 4.13401 1 8 1Z"
                  stroke="#E1A600" stroke-width="2"/>
              <circle cx="8" cy="8" r="2" transform="rotate(-90 8 8)" fill="#E1A600"/>
            </svg>

            <p class="f22 custom-text pl-4">Ускорить время <br>
              исполнения ремонта</p>
          </div>
        </div>
        <div class="col-12 md:col-4">
          <div class="flex align-items-center">
            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                  d="M8 1C11.866 1 15 4.13401 15 8C15 11.866 11.866 15 8 15C4.13401 15 1 11.866 1 8C0.999999 4.13401 4.13401 1 8 1Z"
                  stroke="#E1A600" stroke-width="2"/>
              <circle cx="8" cy="8" r="2" transform="rotate(-90 8 8)" fill="#E1A600"/>
            </svg>

            <p class="f22 custom-text pl-3">
              Избежать множества ошибок <br>
              и сэкономить деньги
            </p>
          </div>
        </div>
        <div class="col-12 md:col-4">
          <div class="flex align-items-center">
            <svg width="16" height="16" viewBox="0 0 16 16" fill="none" xmlns="http://www.w3.org/2000/svg">
              <path
                  d="M8 1C11.866 1 15 4.13401 15 8C15 11.866 11.866 15 8 15C4.13401 15 1 11.866 1 8C0.999999 4.13401 4.13401 1 8 1Z"
                  stroke="#E1A600" stroke-width="2"/>
              <circle cx="8" cy="8" r="2" transform="rotate(-90 8 8)" fill="#E1A600"/>
            </svg>
            <p class="f22 custom-text pl-3">Не тратить нервы <br>
              и время</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="form-footer form-service">
    <div class="container pt-8 pb-5">
      <div class="grid">
        <div class="col-12 md:col-6">
          <img src="http://dom-uyta.ru/img/magazine2.png" class="w-full" alt="">
        </div>
        <div class="col-12 md:col-4 pt-5">
          <div class="flex">
            <div class=""><span class="icon">
                    <svg width="36" height="37" viewBox="0 0 36 37" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <g clip-path="url(#clip0)">
                            <path
                                d="M25.875 18.0015H21.375C20.7536 18.0015 20.25 18.5051 20.25 19.1265V28.1265C20.25 28.7478 20.7536 29.2515 21.375 29.2515H25.875C27.1176 29.2515 28.125 28.2441 28.125 27.0015V20.2515C28.125 19.0088 27.1176 18.0015 25.875 18.0015ZM25.875 27.0015H22.5V20.2515H25.875V27.0015Z"
                                fill="white"/>
                            <path
                                d="M36 20.2515V18.0015H30.375C29.7536 18.0015 29.25 18.5051 29.25 19.1265V29.2515H31.5V24.7515H36V22.5015H31.5V20.2515H36Z"
                                fill="white"/>
                            <path
                                d="M2.25 32.6262V3.37624C2.25 2.75489 2.75365 2.25124 3.375 2.25124H20.25V6.75124C20.25 7.99387 21.2574 9.00124 22.5 9.00124H27V12.3762H29.25V7.87624C29.2518 7.5772 29.1343 7.28976 28.9237 7.07749L22.1737 0.327489C21.9615 0.116903 21.674 -0.000448846 21.375 0.00123865H3.375C1.51102 0.00123865 0 1.51232 0 3.37624V32.6262C0 34.4902 1.51102 36.0012 3.375 36.0012H11.25V33.7512H3.375C2.75372 33.7512 2.25 33.2476 2.25 32.6262Z"
                                fill="white"/>
                            <path
                                d="M16.875 18.0015H12.375C11.7536 18.0015 11.25 18.5051 11.25 19.1265V29.2515H13.5V25.8765H16.875C18.1176 25.8765 19.125 24.8691 19.125 23.6265V20.2515C19.125 19.0088 18.1176 18.0015 16.875 18.0015ZM16.875 23.6265H13.5V20.2515H16.875V23.6265Z"
                                fill="white"/>
                        </g>
                        <defs>
                            <clipPath id="clip0">
                                <rect width="36" height="36" fill="white" transform="translate(0 0.00146484)"/>
                            </clipPath>
                        </defs>
                    </svg>
                </span></div>


            <div class="">
              <div class="mb-3 pl-3 ">
                <p class="input-design__title">Получите пример готового дизайн-проекта</p>
                <p class="custom-text">На WhatsApp моментально, без звонков! </p>
              </div>

              <div class="mb-3 pt-3">
                <input type="text" class="form-control" id="tel" placeholder="Введите ваш телефон" required>
              </div>
              <div class="mb-3 form-check">
                <input type="checkbox" class="check-input " id="exampleCheck1" required checked>
                <label class="custom-text pl-2" for="exampleCheck1">Я согласен на обработку персональных данных</label>
              </div>
              <Button label="получить на whatsapp" severity="warning"
                      class="mt-4 w250px h-50px text-white font-medium mt-5 border-noround text-base uppercase"/>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="service-price ">
    <div class="container pt-6 pb-6">
      <div class="grid">
        <div class="col-12 bamhaeska">
          <div class="grid ">
            <div class="col-4 ">
              <p class="h1">Цены</p>
            </div>
            <div class="col-8">
              <div class="flex justify-content-between align-items-end">
                <div class="head">
                  <div class="text-center text-center head  flex flex-column justify-content-center">
                    <p class="title">Экспресс</p>
                    <p class="price">1200 ₽/м2</p>
                  </div>
                </div>
                <div class=" lead">
                  <div class="lead text-center  flex flex-column justify-content-center">
                    <p class="title text-white">Стандарт</p>
                    <p class="price">2000 ₽/м2</p>
                  </div>
                </div>
                <div class=" head">
                  <div class="text-center head flex flex-column justify-content-center">
                    <p class="title">Все включено</p>
                    <p class="price">2500 ₽/м2</p>
                  </div>
                </div>
              </div>
            </div>
          </div>
          <div class="grid">
            <div class="col-4">
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>
              <div class="check-after__text flex justify-content-start align-items-center">
                <p class="amunition pl-3">Подбор стилистической идеи помещения</p>
              </div>

            </div>
            <div class="col-8 grid">
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>


              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>


              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>


              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center "><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div
                  class="col-12 md:col-4 check text-center center_check h70px flex justify-content-center align-items-center">
                <img
                    src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
              <div class="col-12 md:col-4 check text-center h70px flex justify-content-center align-items-center"><img
                  src="public/checkbox.svg" class="h12px object-cover" alt=""></div>
            </div>
          </div>
          <div class="grid ">
            <div class="col-4"></div>
            <div class="col-8 flex">
              <div class="drop flex align-items-center justify-content-center">
                <Button label="Заказать" severity="secondary"
                        class="border-noround text-xl	font-medium	h60px w-120px" outlined/>
              </div>
              <div class=" w-full energy flex align-items-center justify-content-center">
                <Button label="заказать" severity="warning"
                        class="mt-4  h-60px w-130px  text-white font-medium mt-5 border-noround text-base uppercase"/>
              </div>
              <div class="drop">
                <div class="drop flex align-items-center justify-content-center">
                  <Button label="Заказать" severity="secondary"
                          class="border-noround text-xl	font-medium	h60px w-120px" outlined/>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

  </section>
  <section class="steps">
    <div class="container">
      <div class="grid">
        <div class="col-12 md:col-4">
          <h1 class="custom-title">Этапы работы</h1>
        </div>
        <div class="col-12 md:col-8">
          <div class="steps__block">
            <p class="steps__number ">1</p>
            <p class="steps__text__title uppercase">
              Выезд на объект
            </p>
            <p class="steps__text__subtitle">
              Знакомство, анализ объекта, архитектурных особенностей. Изучаем план БТИ.
            </p>
          </div>
          <div class="steps__block">
            <p class="steps__number ">2</p>
            <p class="steps__text__title uppercase">
              анкета
            </p>
            <p class="steps__text__subtitle ">
              В ходе беседы с Вами, мы определяем предпочтения, пожелания и увлечения. Фиксируем их в виде технического
              задания.
            </p>
          </div>
          <div class="steps__block">
            <p class="steps__number ">3</p>
            <p class="steps__text__title uppercase">
              Проведение замеров
            </p>
            <p class="steps__text__subtitle">
              Знакомство, анализ объекта, архитектурных особенностей. Изучаем план БТИ.
            </p>
          </div>

        </div>
      </div>
    </div>
  </section>
  <section class="sign__up">
    <div class="container z-1 pb-8">
      <div class="content ">
        <div class="grid pt-6">
          <div class="col-12 lg:col-6 pt-7 ">
            <h2 class="text-white sign__up__title">Посетите любой из наших объектов в живую и убедитесь в качестве
              выполняемых нами
              работ!</h2>
            <div class="flex"><p class="font-4xl"><span class="text-4xl">01</span><span class="pet">/03</span></p>
              <p class="span__line mt20px ml-3"></p>
              <p class="span__line1 mt20.5px "></p>
            </div>
            <p class="sign__up__subtitle pr-8">Покажем текущие проекты на разных стадиях: от
              идеи на фото до созданий
              готового
              дизайна</p>
          </div>
          <div class="col-12 lg:col-6 frogy">
            <h2 class="text-white">Записаться на просмотр</h2>
            <input type="text" class="block text-white input mb-4" placeholder="Введите ваше имя">
            <input type="text" class="block text-white input" placeholder="Введите ваш телефон">
            <div class="flex align-items-end mt-4"><input type="checkbox" class="w30px h-20px border-noround  " name=""
                                                          id="">
              <p class="kasha">Я согласен на обработку персональных данных</p></div>
            <Button label="ЗАПИСАТЬСЯ НА ПРОСМОТР" severity="warning"
                    class="mt-4 w250px h-50px text-white font-medium mt-5"/>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="video">
    <div class="container pt-8 pb-6">
      <div class="grid align-items-center">
        <div class="col-12 md:col-6">
          <h2 class="video__title text-white pb-5">Видеообзоры реализованных проектов</h2>
          <p class="video__subtitle">Наша студия реализовала
            более <span class="text-5xl">500</span> проектов в Екатеринбурге</p>
        </div>
        <div class="col-12 md:col-6">
          <div class="grid">
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover"
                                                       src="https://s3-alpha-sig.figma.com/img/8eb0/d488/aefc56fbccc4c2c3430d8e7e855ae56c?Expires=1697414400&Signature=SYa~EtfMmVS6-8LVN7fW~GTh7ZDQbEXRkvvfXfGIpWmegTnA2llh6TwMFIwKskez7eMN34NIkBNZWpLKga3GvtHRrpfPLMn0M03MZ6-QfWEc2iU4X5KmBAUnlzyXlmJJIJbhxLlal1jDoYAA08NEt~e6XSwvAFfMDI2ppJv6ANtOFkTSllJZ~A0FnVc96129Q1wfXxQh7iFcoGl3N5BRfs5v9hzYvUQelsubmJ0WFoRA50w-CR08Tu6s3ghS3AnfU0qQECKlLqKzzPIj91NJMDKlHHMM2D~lkfU~V49atClvvhMKnp4s7Ba6McZaezF6MFaoypCqGGEMiMXX4AnCiA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                                       alt="">
              <a href="https://youtu.be/yp5n5DGPrgI"><img class="iht" src="../public/play_button.png" alt=""></a>
            </div>
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover"
                                                       src="https://s3-alpha-sig.figma.com/img/8eb0/d488/aefc56fbccc4c2c3430d8e7e855ae56c?Expires=1697414400&Signature=SYa~EtfMmVS6-8LVN7fW~GTh7ZDQbEXRkvvfXfGIpWmegTnA2llh6TwMFIwKskez7eMN34NIkBNZWpLKga3GvtHRrpfPLMn0M03MZ6-QfWEc2iU4X5KmBAUnlzyXlmJJIJbhxLlal1jDoYAA08NEt~e6XSwvAFfMDI2ppJv6ANtOFkTSllJZ~A0FnVc96129Q1wfXxQh7iFcoGl3N5BRfs5v9hzYvUQelsubmJ0WFoRA50w-CR08Tu6s3ghS3AnfU0qQECKlLqKzzPIj91NJMDKlHHMM2D~lkfU~V49atClvvhMKnp4s7Ba6McZaezF6MFaoypCqGGEMiMXX4AnCiA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                                       alt="">
              <a href="https://youtu.be/yp5n5DGPrgI"><img class="iht" src="../public/play_button.png" alt=""></a>
            </div>
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover"
                                                       src="https://s3-alpha-sig.figma.com/img/8eb0/d488/aefc56fbccc4c2c3430d8e7e855ae56c?Expires=1697414400&Signature=SYa~EtfMmVS6-8LVN7fW~GTh7ZDQbEXRkvvfXfGIpWmegTnA2llh6TwMFIwKskez7eMN34NIkBNZWpLKga3GvtHRrpfPLMn0M03MZ6-QfWEc2iU4X5KmBAUnlzyXlmJJIJbhxLlal1jDoYAA08NEt~e6XSwvAFfMDI2ppJv6ANtOFkTSllJZ~A0FnVc96129Q1wfXxQh7iFcoGl3N5BRfs5v9hzYvUQelsubmJ0WFoRA50w-CR08Tu6s3ghS3AnfU0qQECKlLqKzzPIj91NJMDKlHHMM2D~lkfU~V49atClvvhMKnp4s7Ba6McZaezF6MFaoypCqGGEMiMXX4AnCiA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                                       alt="">
              <a href="https://youtu.be/yp5n5DGPrgI"><img class="iht" src="../public/play_button.png" alt=""></a>
            </div>
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover"
                                                       src="https://s3-alpha-sig.figma.com/img/8eb0/d488/aefc56fbccc4c2c3430d8e7e855ae56c?Expires=1697414400&Signature=SYa~EtfMmVS6-8LVN7fW~GTh7ZDQbEXRkvvfXfGIpWmegTnA2llh6TwMFIwKskez7eMN34NIkBNZWpLKga3GvtHRrpfPLMn0M03MZ6-QfWEc2iU4X5KmBAUnlzyXlmJJIJbhxLlal1jDoYAA08NEt~e6XSwvAFfMDI2ppJv6ANtOFkTSllJZ~A0FnVc96129Q1wfXxQh7iFcoGl3N5BRfs5v9hzYvUQelsubmJ0WFoRA50w-CR08Tu6s3ghS3AnfU0qQECKlLqKzzPIj91NJMDKlHHMM2D~lkfU~V49atClvvhMKnp4s7Ba6McZaezF6MFaoypCqGGEMiMXX4AnCiA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                                       alt="">
              <a href="https://youtu.be/yp5n5DGPrgI"><img class="iht" src="../public/play_button.png" alt=""></a>
            </div>
          </div>
        </div>
      </div>
    </div>

  </section>
  <section class="reviews">
    <div class="container pb-8">
      <div class="grid">
        <div class="col-12 md:col-4 lamp">
          <img class="w-full h594px object-cover" src="https://dom-uyta.ru/img/lamp.png" alt="">
        </div>
        <div class="col-12 md:col-8 pr-8">
          <h2 class="text-white pb-7">Вопрос-ответ</h2>
          <div class="">
            <div class="flex justify-content-between ">
              <div class="">
                <p class="reviews__questions">Когда готовы приступить к работе?</p>
              </div>
              <div class="">
                <i class="pi pi-angle-down" style="font-size: 2rem" v-if="show==true" @click="show = false"></i>
                <i class="pi pi-angle-up" style="font-size: 2rem" v-if="show==false" @click="show = true"></i>

              </div>
            </div>
            <div class="reviews__line mt-4"></div>
            <div class="pt-4" v-if="show">
              <p class="reviews__answers">С момента подписания договора в течении 3-5 дней мы приступаем к работам</p>
            </div>
          </div>
          <div class="pt-6">
            <div class="flex justify-content-between">
              <div class="">
                <p class="reviews__questions">Есть ли возможность оплаты безналом?</p>
              </div>
              <div class="">
                <i class="pi pi-angle-down" style="font-size: 2rem" v-if="show2==true" @click="show2 = false"></i>
                <i class="pi pi-angle-up" style="font-size: 2rem" v-if="show2==false" @click="show2 = true"></i>

              </div>
            </div>
            <div class="reviews__line mt-4"></div>
            <div class="pt-4" v-if="show2">
              <p class="reviews__answers">Да. Оплаты производятся удобным для вас способом. По счету через банк, по
                терминалу или при необходимости от юр. лица.</p>
            </div>
          </div>
          <div class="pt-6">
            <div class="flex justify-content-between">
              <div class="">
                <p class="reviews__questions">Кто у Вас работает?</p>
              </div>
              <div class="">
                <i class="pi pi-angle-down" style="font-size: 2rem" v-if="show3==true" @click="show3 = false"></i>
                <i class="pi pi-angle-up" style="font-size: 2rem" v-if="show3==false" @click="show3 = true"></i>

              </div>
            </div>
            <div class="reviews__line mt-4"></div>
            <div class="pt-4" v-if="show3">
              <p class="reviews__answers">У нас работают только граждане РФ. Действует разделение труда: Электрики,
                сантехники, отделочники (маляры, плиточники). В результате качество работ остается на должном уровне и
                работы продвигаются быстрее, ведь каждый сотрудник выполняет работу которую умеет делать лучше
                всего.</p>
            </div>
          </div>
          <div class="pt-6">
            <div class="flex justify-content-between">
              <div class="">
                <p class="reviews__questions">Может ли измениться стоимость работ?</p>
              </div>
              <div class="">
                <i class="pi pi-angle-down" style="font-size: 2rem" v-if="show4==true" @click="show4 = false"></i>
                <i class="pi pi-angle-up" style="font-size: 2rem" v-if="show4==false" @click="show4 = true"></i>

              </div>
            </div>
            <div class="reviews__line mt-4"></div>
            <div class="pt-4" v-if="show4">
              <p class="reviews__answers">Нет. Наши сметы фиксированны и мы несем ответственность за их точность в
                соответствии с вашими потребностями, дополнительные работы и увеличение сметной стоимости исключены.
                Только если они не возникли в результате ваших дополнительных пожеланий по ремонту в процессе.</p>
            </div>
          </div>
          <div class="pt-6">
            <div class="flex justify-content-between">
              <div class="">
                <p class="reviews__questions">Помогаете ли вы с приобретением чистовых материалов?</p>
              </div>
              <div class="">
                <i class="pi pi-angle-down" style="font-size: 2rem" v-if="show5==true" @click="show5 = false"></i>
                <i class="pi pi-angle-up" style="font-size: 2rem" v-if="show5==false" @click="show5 = true"></i>

              </div>
            </div>
            <div class="pt-4" v-if="show5">
              <p class="reviews__answers">Да. У нас работает отдел комплектации и есть собственный магазин отделочных
                материалов. Мо можем помочь вам с подбором абсолютно всех материалов: напольных покрытий, плитки,
                керамогранита, обоев, сантехники, светильников и др. Так же можем сделать бесплатный дизайн проект
                ванной комнаты.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="questions">
    <!--    <div class="line3"></div>-->
    <div class="container pb-8 lera ">
      <div class="grid pt-6">
        <div class="col-12 lg:col-6 pt-7 ">
          <h2 class="text-white pb-4">
            Остались вопросы?<br>
            Спросите специалиста</h2>
          <p class="sign__up__subtitle pr-8 text-white">Закажите бесплатную консультацию,
            и через 5 минут с вами свяжется специалист</p>
        </div>
        <div class="col-12 lg:col-6 frogy">
          <h2 class="text-white">Бесплатная консультация</h2>
          <input type="text" class="block text-white input mb-4" placeholder="Введите ваше имя">
          <input type="text" class="block text-white input" placeholder="Введите ваш телефон">
          <div class="flex align-items-end mt-4"><input type="checkbox" class="w30px h-20px border-noround  " name=""
                                                        id="">
            <p class="kasha text-white">Я согласен на обработку персональных данных</p></div>
          <Button label="получить консультацию" severity="warning"
                  class="mt-4 w250px h-50px text-white font-medium mt-5"/>
        </div>
      </div>
    </div>
  </section>
  <section id="contacts" class="contacts">
    <div class="container pb-6 pt-5">
      <div class="grid">
        <div class="col-12 md:col-6">
          <div class="grid align-items-end">
            <div class="col-12 lg:col-8">
              <p class="contacts__title text-white">Контакты</p>
              <p class="bold pt-5 pb-2 contacts__subtitle">
                Свяжитесь с нами
              </p>
              <p class="text">
                <span class="mgo-number contacts__text" id="call_tel"> +7 (343) 288-58-13</span>
                <br>
                <p class="contacts__text">info@dom-uyta.ru</p>
              </p>
              <p class="pt-5 pb-2 bold contacts__subtitle">
                Наш адрес
              </p>
              <p class="contacts__text">
                г. Екатеринбург, Шевченко, 20
                <br>
                Режим работы: 10:00-21:00
              </p>
            </div>
            <div class="col-12 lg:col-4">
              <div class="box">
                <div class="block flex align-items-center justify-content-end">
                  <div class="">
                    <a href="https://www.instagram.com/dom_uyta_ekb/" target="_blank">
                      <svg width="29" fill="white" xmlns="" viewBox="0 0 448 512">
                        <path
                            d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"/>
                      </svg>
                    </a>
                  </div>
                  <div class="ratatui">
                    <a href="https://vk.com/dom_uyta_ekb" target="_blank">
                      <svg width="29" height="31" viewBox="0 0 29 31" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M27.4537 7.94922C27.6554 7.28828 27.4537 6.80781 26.5616 6.80781H23.5954C22.8471 6.80781 22.5016 7.22852 22.3 7.67852C22.3 7.67852 20.7741 11.5223 18.6433 14.0143C17.9522 14.735 17.6356 14.9752 17.2612 14.9752C17.0596 14.9752 16.8002 14.735 16.8002 14.0746V7.91816C16.8002 7.1377 16.5702 6.77734 15.9364 6.77734H11.2715C10.8104 6.77734 10.5227 7.1377 10.5227 7.49805C10.5227 8.24863 11.5881 8.4291 11.7031 10.5309V15.0977C11.7031 16.0885 11.5332 16.2695 11.1559 16.2695C10.1483 16.2695 7.70086 12.3959 6.23273 7.98203C5.94727 7.10781 5.65727 6.77734 4.90848 6.77734H1.91389C1.05012 6.77734 0.90625 7.19746 0.90625 7.64805C0.90625 8.45898 1.91389 12.5424 5.59949 17.9471C8.04693 21.6385 11.5309 23.6225 14.6694 23.6225C16.5702 23.6225 16.8002 23.1719 16.8002 22.4213V19.6287C16.8002 18.7281 16.9729 18.5781 17.5779 18.5781C18.0095 18.5781 18.7871 18.8178 20.5436 20.5896C22.5588 22.6914 22.9043 23.6523 24.0275 23.6523H26.9932C27.857 23.6523 28.2603 23.2018 28.0297 22.3311C27.7709 21.4604 26.7916 20.1994 25.5245 18.6982C24.8335 17.858 23.797 16.927 23.4804 16.4764C23.0488 15.8758 23.1637 15.6355 23.4804 15.0953C23.4515 15.0953 27.0799 9.75039 27.4537 7.94688"
                            stroke="white" stroke-width="1.5"/>
                      </svg>
                    </a>
                  </div>
                  <div class="">
                    <a href="https://www.youtube.com/channel/UCxLEk30TG5qJH-2yps0M8kw" target="_blank">
                      <svg width="29" height="23" viewBox="0 0 29 23" fill="none" xmlns="http://www.w3.org/2000/svg">
                        <path
                            d="M27.8231 6.1735C27.8231 3.80045 26.0776 1.89146 23.9208 1.89146C20.9993 1.75488 18.0198 1.70215 14.9749 1.70215H14.0257C10.9882 1.70215 8.00345 1.75488 5.08196 1.89199C2.9304 1.89199 1.18489 3.81152 1.18489 6.18457C1.05306 8.06139 0.997157 9.93873 1.00032 11.8161C0.995047 13.6934 1.05481 15.5725 1.17962 17.4534C1.17962 19.8264 2.92513 21.7512 5.07669 21.7512C8.14583 21.8936 11.2941 21.9569 14.495 21.9516C17.7013 21.9622 20.8407 21.8954 23.9134 21.7512C26.0702 21.7512 27.8157 19.8264 27.8157 17.4534C27.9423 15.5708 28.0003 13.6934 27.995 11.8108C28.007 9.93346 27.9497 8.05436 27.8231 6.1735ZM11.9163 16.9893V6.62701L19.5628 11.8055L11.9163 16.9893Z"
                            stroke="white" stroke-width="1.5"/>
                      </svg>
                    </a>
                  </div>
                </div>
                <div class="flex text-center rety">
                  <div class="bottom">
                    <p class="contacts__subtitle">нажми</p>
                    <a href="https://www.instagram.com/dom_uyta_ekb/" target="_blank">
                      <img class=" h150px"
                           src="https://s3-alpha-sig.figma.com/img/c1fb/68ce/76ceb5e70faa57b5caf0008993d249a6?Expires=1698019200&Signature=mK03AnDqd0R9r0zWFB6R7s2Eh2f3I1Me8d6oPmuKXRe~R~nWejvNHBgjqUIdhd4jSppvXvs~cFhr1TusXxAzhafL7elHovafa80JOVrUyX0yoQP4O6wpvsaM4V6N~zI3aU9o5ghkIIOjfIdaj4A9TJYD8-Qea93Ju8s-CmtwswWyqUU0nnBAStY-jyewOKkc5PFi8E5VPvf-uCHTmGZYGVtIgZfSqOANilsg4GeomRWPiEKst6V2~21s79ynR50iW3X-CYNeCDOp6g8L0PlxuqzyvjH9Nk07dV-iZ7Pnhsv83AmCwSteDqghENDLrm7lDumJ4Pdx8IPx1jBgIg54HQ__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4">
                    </a>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 pl-5">
          <img class="w-full h-full border-round-sm ml-2 object-cover"
               src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS2hMP2IvkyBI7PkV7jvyq_xifKdpetbGABO_7C5kIztg&s"
               alt="">
        </div>
      </div>
    </div>
  </section>
  <footer class="footer">
    <div class="container pt-6">
      <div class="grid">
        <div class="col-6 md:col-8">
          <div class="grid">
            <div class="col-12 md:col-4">
              <p><a href="#" class="nav-link p-0 f22 footer__subtitle">Услуги</a></p>
              <ul class="nav flex-column p-0 faght">
                <li class="nav-item mb-2"><a href="/design/" class="nav-link p-0 footer__text">Дизайн интерьера</a></li>
                <li class="nav-item mb-2"><a href="/remont/" class="nav-link p-0 footer__text">Ремонтные работы</a></li>
                <li class="nav-item mb-2"><a href="/cottages/" class="nav-link p-0 footer__text">Строительство
                  коттеджей</a></li>
                <li class="nav-item mb-2"><a href="/equipment/" class="nav-link p-0 footer__text">Комплектация
                  проектов</a></li>
                <li class="nav-item mb-2"><a href="#" class="nav-link p-0 footer__text">Натяжные потолки и
                  остекление</a></li>
              </ul>
            </div>
            <div class="col-12 md:col-4">
              <p><a href="/portfolio/" class="nav-link p-0 f22 footer__subtitle">Портфолио</a></p>
              <ul class="nav flex-column p-0  faght">
                <li class="nav-item mb-2"><a href="/portfolio/" class="nav-link p-0 footer__text">Дизайн интерьера</a>
                </li>
                <li class="nav-item mb-2"><a href="/portfolio/" class="nav-link p-0 footer__text">Ремонтные работы</a>
                </li>
                <li class="nav-item mb-2"><a href="/portfolio/" class="nav-link p-0 footer__text">Строительство
                  коттеджей</a></li>
                <li class="nav-item mb-2"><a href="/portfolio/" class="nav-link p-0 footer__text">Видеообзоры</a></li>
              </ul>
            </div>
            <div class="col-12 md:col-4">
              <p><a href="/about/" class="nav-link p-0 f22 footer__subtitle">О компании</a></p>
              <p><a href="#" class="nav-link p-0 f22 footer__text">Контакты</a></p>
              <div class="grid">
                <div class="col-4">
                  <a href="https://www.instagram.com/dom_uyta_ekb/" target="_blank">
                    <svg width="29" fill="white" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">
                      <!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. -->
                      <path
                          d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z"/>
                    </svg>
                  </a>
                </div>
                <div class="col-4">
                  <a href="https://vk.com/dom_uyta_ekb" target="_blank">
                    <svg width="29" height="31" viewBox="0 0 29 31" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <path
                          d="M27.4537 7.94922C27.6554 7.28828 27.4537 6.80781 26.5616 6.80781H23.5954C22.8471 6.80781 22.5016 7.22852 22.3 7.67852C22.3 7.67852 20.7741 11.5223 18.6433 14.0143C17.9522 14.735 17.6356 14.9752 17.2612 14.9752C17.0596 14.9752 16.8002 14.735 16.8002 14.0746V7.91816C16.8002 7.1377 16.5702 6.77734 15.9364 6.77734H11.2715C10.8104 6.77734 10.5227 7.1377 10.5227 7.49805C10.5227 8.24863 11.5881 8.4291 11.7031 10.5309V15.0977C11.7031 16.0885 11.5332 16.2695 11.1559 16.2695C10.1483 16.2695 7.70086 12.3959 6.23273 7.98203C5.94727 7.10781 5.65727 6.77734 4.90848 6.77734H1.91389C1.05012 6.77734 0.90625 7.19746 0.90625 7.64805C0.90625 8.45898 1.91389 12.5424 5.59949 17.9471C8.04693 21.6385 11.5309 23.6225 14.6694 23.6225C16.5702 23.6225 16.8002 23.1719 16.8002 22.4213V19.6287C16.8002 18.7281 16.9729 18.5781 17.5779 18.5781C18.0095 18.5781 18.7871 18.8178 20.5436 20.5896C22.5588 22.6914 22.9043 23.6523 24.0275 23.6523H26.9932C27.857 23.6523 28.2603 23.2018 28.0297 22.3311C27.7709 21.4604 26.7916 20.1994 25.5245 18.6982C24.8335 17.858 23.797 16.927 23.4804 16.4764C23.0488 15.8758 23.1637 15.6355 23.4804 15.0953C23.4515 15.0953 27.0799 9.75039 27.4537 7.94688"
                          stroke="white" stroke-width="1.5"/>
                    </svg>
                  </a>
                </div>
                <div class="col-4">
                  <a href="https://www.youtube.com/channel/UCxLEk30TG5qJH-2yps0M8kw" target="_blank">
                    <svg width="29" height="23" viewBox="0 0 29 23" fill="none" xmlns="http://www.w3.org/2000/svg">
                      <path
                          d="M27.8231 6.1735C27.8231 3.80045 26.0776 1.89146 23.9208 1.89146C20.9993 1.75488 18.0198 1.70215 14.9749 1.70215H14.0257C10.9882 1.70215 8.00345 1.75488 5.08196 1.89199C2.9304 1.89199 1.18489 3.81152 1.18489 6.18457C1.05306 8.06139 0.997157 9.93873 1.00032 11.8161C0.995047 13.6934 1.05481 15.5725 1.17962 17.4534C1.17962 19.8264 2.92513 21.7512 5.07669 21.7512C8.14583 21.8936 11.2941 21.9569 14.495 21.9516C17.7013 21.9622 20.8407 21.8954 23.9134 21.7512C26.0702 21.7512 27.8157 19.8264 27.8157 17.4534C27.9423 15.5708 28.0003 13.6934 27.995 11.8108C28.007 9.93346 27.9497 8.05436 27.8231 6.1735ZM11.9163 16.9893V6.62701L19.5628 11.8055L11.9163 16.9893Z"
                          stroke="white" stroke-width="1.5"/>
                    </svg>
                  </a>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div class="col-6 md:col-4">
          <div class="flex justify-content-end"><img
              src="https://s3-alpha-sig.figma.com/img/ec52/8067/7f26f9c96db219bc8a13d405a53c4e59?Expires=1698019200&Signature=hT9o17315q7nG3t~BQDEZBsxciyafuDZJloopg1NPLU51Au2CMjIhoaLN3NJcaB1lOpc64Z4dfbFz8B01JAyY29NkBawbVOiEdHK9pfDYxTu2Ltiq9faVjIZrhl1TW-4Zrp-miP3tz~7QABH4ugWIjbWdU9C9cwAxONo30KGKBlE8zwJohiWP-xtMBpLoJGjSiv~0xbecwwusFHrN01GhmsHoWjxIwhq4scwVwrO~p~WwO5qPR7~~ynfkVyrhuM5Xp~2j4e1u9bAW3-vrjoIpnO3k1IcLcKcIqWIqsAPNO4BKPpwL0De6xKUumfglIuAiEqAgzYpbUvQsqdXLhQlZw__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
              class="w-130px h80px " alt=""></div>
          <div class="clearfix"></div>
          <p class="text-end">
            <span class="mgo-number footer__text" id="call_tel">+7 (343) 288-58-13</span>
            <br>
            <p class="footer__text text-end">info@dom-uyta.ru</p>
          </p>
          <p class="text-end footer__text">
            г. Екатеринбург, Шевченко, 20
            <br>
            Режим работы: 10:00-21:00
          </p>
        </div>
      </div>
      <div class="grid copyright">
        <div class="col-12 md:col-3">
          <p class="footer__confidencial">
            © 2015 - 2023 Дом-Уюта
            <br>
            информация на сайте не является публичной офертой
          </p>
        </div>
        <div class="col-12 md:col-3">
          <p class="footer__confidencial">
            Политика конфиденциальности
          </p>
        </div>
        <div class="col-12 md:col-3">
          <p>
            <a href="/personal-information.php " class="footer__confidencial">Согласие на обработку персональных
              данных</a>
          </p>
        </div>
      </div>
    </div>
  </footer>
</template>
<style>
.banner02 {
  display: none;
  @media screen and (max-width: 768px) {
    display: block;
    background-image: url("http://dom-uyta.ru/upload/resize_cache/iblock/2fb/1000_750_2/2fb0252998c2693e974bb4d53211528f.jpg");
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
    width: 100%;
    height: 100%;
  }
}

.btn__text {
  color: #FFF;
  text-align: center;
  font-size: 11px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  background-color: #3d3e45;
  border: none;
}

.li {
  position: relative;
}

.li:before {
  content: '';
  position: absolute;
  top: 15px;
  left: 0;
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background-color: white;
}

.banner__text {
  color: #FFF;

  /* Body */
  font-size: 13px;
  font-style: normal;
  font-weight: 300;
  line-height: 135%; /* 21.6px */
}

.banner__title {
  font-family: "Playfair Display", serif;
  font-weight: 900;
  font-size: 32px;
}

.banner {
  background-color: #23242a;
  width: 100%;
  height: 100%;
  @media screen and (max-width: 768px) {
    display: none;
  }
}

.steps__text__title {
  position: absolute;
  top: 100px;
  left: 40px;
  color: var(--color-styles-white, #FFF);
  font-feature-settings: 'clig' off, 'liga' off;
  font-family: Gilroy;
  font-size: 36px;
  font-style: normal;
  font-weight: 600;
  line-height: 56px; /* 155.556% */
  @media screen and (max-width: 1041px) {
    top: 60px;
  }
}

.steps__text__subtitle {
  color: var(--color-styles-white, #FFF);
  font-feature-settings: 'clig' off, 'liga' off;

  /* Body */
  font-family: Gilroy;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 135%; /* 21.6px */
  position: absolute;
  top: 170px;
  left: 40px;
}

.steps__number {
  font-feature-settings: 'clig' off, 'liga' off;
  font-family: Playfair Display;
  font-size: 166px;
  font-style: normal;
  font-weight: 900;
  line-height: 135%; /* 224.1px */
}

.steps__block {
  position: relative;
}

.steps {
  background-color: #353840;
  width: 100%;
  height: auto;
}

.bamhaeska {
  @media screen and (max-width: 768px) {
    display: none;
  }
}

.energy {
  background: #FBFCFE;
  width: 100%;
  height: 150px;
}

.drop {
  background: #FBFCFE;
  width: 100%;
  height: 130px;
}

.amunition {
  color: #FFF;
  font-size: 15px;
  font-style: normal;
  font-weight: 300;
  line-height: 16px; /* 106.667% */
}

.check-after__text {
  background: #2a2c33;
  width: 100%;
  height: 70px;
}

.center_check {
  border: 1px solid #f9fafc;
}

.check {
  background: #FBFCFE;
}

.col-4 {
  padding: 0px;
}

.col-8 {
  padding-bottom: 0px;
  margin-bottom: 0px;
  padding-left: 0px;
  margin-left: 0px;
}

.lead {
  background: var(--gold, #E1A600);
  width: 100%;
  height: 145px;
}

.head {
  background: #FBFCFE;
  width: 100%;
  height: 130px;
}

.price {
  color: var(--light, #3D3E45);
  text-align: center;
  font-family: Gilroy;
  font-size: 21px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
}

.title {
  color: #464855;
  text-align: center;
  font-size: 23px;
  font-style: normal;
  font-weight: 300;
  line-height: 32px; /* 114.286% */
}

.h1 {
  color: #FFF;
  font-feature-settings: 'clig' off, 'liga' off;
  font-family: Playfair Display;
  font-size: 45px;
  font-style: normal;
  font-weight: 900;
  line-height: 135%; /* 70.2px */
}

.service-price {
  background-color: #353840;
  width: 100%;
  height: auto;
}

.input-design__title {
  color: var(--color-styles-white, #FFF);
  font-feature-settings: 'clig' off, 'liga' off;
  font-size: 26px;
  font-weight: 700;
  line-height: 39.5px; /* 119.697% */
}

.form-control {
  background: #4b4d54;
  border: none;
  width: 100%;
  height: 35px;
  border-radius: 5px;
  padding-left: 5px;
}

.form-footer {
  background-color: #383a43;
  width: 100%;
  height: 100%;
}

.service-promo {
  background-color: #353840;
  width: 100%;
  height: auto;
}

.content1 {
  background-color: #23242a;
  width: 100%;
  height: auto;
}

.service-content {
  background-color: #23242a;
  width: 100%;
  height: auto;
}

.custom-title {
  color: var(--color-styles-white, #FFF);
  font-feature-settings: 'clig' off, 'liga' off;

  /* H3 */
  font-size: 38px;
  font-style: normal;
  font-weight: 600;
  line-height: 56px; /* 116.667% */
}

.custom-text {
  color: var(--color-styles-white, #FFF);
  font-feature-settings: 'clig' off, 'liga' off;

  /* big body */
  font-size: 18px;
  font-style: normal;
  font-weight: 200;
  line-height: 135%; /* 29.7px */
}

.col-12 {
  padding-right: 0px;
  padding-left: 0px;
}

.col-4 {
  padding: 0px;
}

.col-8 {
  padding-bottom: 0px;
  margin-bottom: 0px;
  padding-left: 0px;
  margin-left: 0px;
}
</style>






