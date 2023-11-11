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

  <header class="conection ">
    <div class="blocking">
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
            <p class="dropdown__items1">
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
        <h1 class="banner__title text-white pt-8">Ремонтные <br>
          работы под ключ</h1>
        <p class="banner__text pt-3">Доверив нам ремонт и дизайн жилья,
          Вы будете уверены, что в установленный срок получите квартиру или дом своей мечты.</p>
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
          <router-link to="contacts" class="extra__text pt-2 ">контакты</router-link>
        </p>
        <div class="flex pt-3">
          <img src="public/logo-instagram%202.png" class="pr-5 object-cover h30px " alt="">
          <Button label="связаться" class="w130px h-40px border-noround bg-gray border-none alfa"
                  severity="secondary" raised/>
        </div>
      </div>
    </div>
  </header>
  <section class="design__project">
    <div class="service-content ">
      <div class="container ">
        <div class="grid pt-3 ">
          <div class="col-12">
            <p class="custom-title pb-8">
              Вот что включено в услугу <br> экспертного ремонта:
            </p>
          </div>
        </div>
        <div class="grid">
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="58" height="62" viewBox="0 0 58 62" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M46.318 8.39487V2H2V14.7897H46.318V8.39487ZM46.318 8.39487H55.6872V23.8615H28.3231V32.3385M28.3231 32.3385H33.6769V60H24.3077V32.3385H28.3231Z"
                    stroke="white" stroke-width="4"/>
              </svg>
            </div>
            <p class="custom-text">
              Ремонтно- <br>
              отделочные работы
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
              Технический надзор, <br>
              снабжение и логистика
            </p>
          </div>
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="71" height="61" viewBox="0 0 71 61" fill="none" xmlns="http://www.w3.org/2000/svg">
                <mask id="path-1-outside-1" maskUnits="userSpaceOnUse" x="0" y="0.812988" width="71" height="60"
                      fill="black">
                  <rect fill="white" y="0.812988" width="71" height="60"/>
                  <path d="M36.5952 42.5134V57.3377H38.7857V42.5134H36.5952Z"/>
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M69.009 59.2109H1.99101C1.72818 59.2109 1.47611 59.1123 1.29026 58.9368C1.10441 58.7613 1 58.5233 1 58.2751V2.7488C1 2.50061 1.10441 2.26258 1.29026 2.08708C1.47611 1.91158 1.72818 1.81299 1.99101 1.81299H62.1375C62.4003 1.81299 62.6524 1.91158 62.8382 2.08708C63.0241 2.26258 63.1285 2.50061 63.1285 2.7488V30.4346H69.0081C69.2707 30.4344 69.5226 30.5325 69.7085 30.7075C69.8945 30.8825 69.9993 31.12 70 31.368V58.2751C70 58.5233 69.8956 58.7613 69.7097 58.9368C69.5239 59.1123 69.2718 59.2109 69.009 59.2109ZM17.0606 57.3377V52.9071H9.19375C8.93092 52.9071 8.67885 52.8085 8.493 52.633C8.30715 52.4575 8.20274 52.2194 8.20274 51.9712V35.6821H2.98375L2.98289 57.3377H17.0606ZM2.98289 33.8081H8.20446H10.1865V51.0346H18.0516C18.3145 51.0346 18.5665 51.1332 18.7524 51.3087C18.9382 51.4842 19.0426 51.7222 19.0426 51.9704L19.0435 57.3377H38.7857H68.0163V32.3078H43.8176C43.5548 32.3078 43.3027 32.2092 43.1169 32.0337C42.931 31.8582 42.8266 31.6202 42.8266 31.372V29.5656H40.378V27.6923H42.8258V21.6385H44.8095V30.4346H51.1992H53.1813H54.0095H55.7345H61.1456V3.68542H55.7345H54.0095H53.1813H51.1992H48.5065V12.249H46.5228V9.38128H30.94C30.6771 9.38128 30.4251 9.28269 30.2392 9.10719C30.0534 8.93169 29.9489 8.69366 29.9489 8.44547V3.68542H26.3265H24.3427H23.2732H21.286H16.5975H14.6154H11.0128H9.02988H2.98375V15.1481V17.0205V21.9512V24.1494L2.98289 33.8081ZM31.931 7.50885H46.5236V3.68542H31.931V7.50885Z"/>
                  <path
                      d="M11.0128 16.0847V3.68542H9.02988V15.1481H7.74216H2.98375V17.0205H6.75029H8.73317H10.0218C10.2846 17.0205 10.5367 16.9219 10.7225 16.7464C10.9084 16.5709 11.0128 16.3329 11.0128 16.0847Z"/>
                  <path
                      d="M24.3444 17.9604V22.277L2.98375 21.9512V24.1494H8.20446H10.1865H24.3453V34.1534H26.329V29.5664H28.7725V27.6931H26.3282V17.9604H24.3444Z"/>
                  <path d="M55.7345 30.4346V3.68542H54.0095V30.4346H55.7345Z"/>
                </mask>
                <path d="M36.5952 42.5134V57.3377H38.7857V42.5134H36.5952Z" fill="white"/>
                <path fill-rule="evenodd" clip-rule="evenodd"
                      d="M69.009 59.2109H1.99101C1.72818 59.2109 1.47611 59.1123 1.29026 58.9368C1.10441 58.7613 1 58.5233 1 58.2751V2.7488C1 2.50061 1.10441 2.26258 1.29026 2.08708C1.47611 1.91158 1.72818 1.81299 1.99101 1.81299H62.1375C62.4003 1.81299 62.6524 1.91158 62.8382 2.08708C63.0241 2.26258 63.1285 2.50061 63.1285 2.7488V30.4346H69.0081C69.2707 30.4344 69.5226 30.5325 69.7085 30.7075C69.8945 30.8825 69.9993 31.12 70 31.368V58.2751C70 58.5233 69.8956 58.7613 69.7097 58.9368C69.5239 59.1123 69.2718 59.2109 69.009 59.2109ZM17.0606 57.3377V52.9071H9.19375C8.93092 52.9071 8.67885 52.8085 8.493 52.633C8.30715 52.4575 8.20274 52.2194 8.20274 51.9712V35.6821H2.98375L2.98289 57.3377H17.0606ZM2.98289 33.8081H8.20446H10.1865V51.0346H18.0516C18.3145 51.0346 18.5665 51.1332 18.7524 51.3087C18.9382 51.4842 19.0426 51.7222 19.0426 51.9704L19.0435 57.3377H38.7857H68.0163V32.3078H43.8176C43.5548 32.3078 43.3027 32.2092 43.1169 32.0337C42.931 31.8582 42.8266 31.6202 42.8266 31.372V29.5656H40.378V27.6923H42.8258V21.6385H44.8095V30.4346H51.1992H53.1813H54.0095H55.7345H61.1456V3.68542H55.7345H54.0095H53.1813H51.1992H48.5065V12.249H46.5228V9.38128H30.94C30.6771 9.38128 30.4251 9.28269 30.2392 9.10719C30.0534 8.93169 29.9489 8.69366 29.9489 8.44547V3.68542H26.3265H24.3427H23.2732H21.286H16.5975H14.6154H11.0128H9.02988H2.98375V15.1481V17.0205V21.9512V24.1494L2.98289 33.8081ZM31.931 7.50885H46.5236V3.68542H31.931V7.50885Z"
                      fill="white"/>
                <path
                    d="M11.0128 16.0847V3.68542H9.02988V15.1481H7.74216H2.98375V17.0205H6.75029H8.73317H10.0218C10.2846 17.0205 10.5367 16.9219 10.7225 16.7464C10.9084 16.5709 11.0128 16.3329 11.0128 16.0847Z"
                    fill="white"/>
                <path
                    d="M24.3444 17.9604V22.277L2.98375 21.9512V24.1494H8.20446H10.1865H24.3453V34.1534H26.329V29.5664H28.7725V27.6931H26.3282V17.9604H24.3444Z"
                    fill="white"/>
                <path d="M55.7345 30.4346V3.68542H54.0095V30.4346H55.7345Z" fill="white"/>
              </svg>
            </div>
            <p class="custom-text">
              Проектирование <br>
              инженерных систем
            </p>
          </div>
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="59" height="67" viewBox="0 0 59 67" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M38.8757 0H19.4378V6.34476H38.8757V0ZM25.9171 41.2409H32.3964V22.2067H25.9171V41.2409ZM51.9314 20.2398L56.5317 15.735C55.1386 14.1171 53.616 12.5943 51.9638 11.262L47.3635 15.7667C42.3421 11.833 36.0248 9.48542 29.1567 9.48542C13.0557 9.48542 0 22.2701 0 38.0368C0 53.8036 13.0233 66.5883 29.1567 66.5883C45.2901 66.5883 58.3135 53.8036 58.3135 38.0368C58.3135 31.3431 55.9161 25.157 51.9314 20.2398ZM29.1567 60.2752C16.6193 60.2752 6.47928 50.3457 6.47928 38.0686C6.47928 25.7915 16.6193 15.8619 29.1567 15.8619C41.6941 15.8619 51.8342 25.7915 51.8342 38.0686C51.8342 50.3457 41.6941 60.2752 29.1567 60.2752Z"
                    fill="white"/>
              </svg>
            </div>
            <p class="custom-text">
              Подробный график работ <br>
              и соблюдение сроков
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
        <div class="col-12 md:col-6 pl-5">
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
          <p class="custom-title text-center pb-5">Избавим от лишних хлопот:</p>
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

            <p class="f22 custom-text pl-4">Фиксированная смета <br>
              и официальный договор</p>
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
              Гарантия 3 года
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
            <p class="f22 custom-text pl-3">
              Индивидуальный прораб <br>
              и проект-менеджер</p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="form-footer form-service">
    <div class="container pt-8 pb-5">
      <div class="grid">
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
        <div class="col-12 md:col-8 ">
          <div class="flex justify-content-end">
            <img src="http://dom-uyta.ru/img/37705122.png" class="w-full" alt="">
          </div>
        </div>

      </div>
    </div>
  </section>
  <section class="service-price">
    <div class="container">
      <p class="h1 pb-5 pt-5">Цены</p>

      <div class="grid pt-8">
        <div class="col-12 md:col-4  pb-4">
          <div class="head text-center">
            <div class="price__title pt-4 pb-3 ">
              Базовый ремонт
            </div>
            <div class="price pb-3">
              7 000 ₽/м2
            </div>
            <div class="flex align-items-center justify-content-center pt-2">
            <span class="time flex align-items-center justify-content-center wow surface-200	">
                        <img src="public/Icon-Timer.png" alt="">
                        <p style="color:#999999; font-size: 13px;">от 30 дней</p>
                    </span>
            </div>
            <div class="pt-7">
              <div class="usligi__text flex justify-content-start align-items-center">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Шпатлевание и окраска стен</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Укладка керамической плитки сан. узел</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Переустройство и монтаж сантехники</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Монтаж новых розеток/выключателей</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Укладка напольных покрытий и плинтусов</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3 pb-5">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Монтаж натяжного потолка</p>
              </div>
            </div>

            <div class=" text-center pt-8 pb-8">
              <Button label="Заказать" severity="secondary"
                      class="price__btn border-noround" outlined/>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-4  kot ">
          <div class="head text-center">
            <div class="price__title pt-4 pb-3 ">
              Капитальный ремонт
            </div>
            <div class="price pb-3">
              10 000 ₽/м2
            </div>
            <div class="flex align-items-center justify-content-center pt-2">
            <span class="time flex align-items-center justify-content-center wow surface-200	">
                        <img src="public/Icon-Timer.png" alt="">
                        <p style="color:#999999; font-size: 13px;">от 10 дней</p>
                    </span>
            </div>
            <div class="pt-7">
              <div class="usligi__text flex justify-content-start align-items-center">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Перепланировка</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Согласование перепланировки</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Новая разводка электрики и сантехники</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Выравнивание поверхностей стен и полов</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Шпатлевание и окраска стен</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3 ">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Укладка напольных покрытий</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3 ">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Укладка напольных покрытий</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3 ">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Укладка керамической плитки сан.узел</p>
              </div>
              <div class="usligi__text flex justify-content-start align-items-center pt-3 pb-5">
                <img src="public/Available__mark.png" class="pl-5" alt="">
                <p class=" pl-2">Монтаж натяжного потолка</p>
              </div>
            </div>

            <div class=" text-center  pb-8">
              <Button label="Заказать" severity="secondary"
                      class="price__btn border-noround" outlined/>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-4  ">
          <div class="lead text-center">
            <div class="title ghoki pt38px text-white">
              По дизайн-проекту
              <div class="price pt-3">
                12 000 ₽/м2
              </div>
              <span class="time flex justify-content-center align-items-center pt-3 pb-2">
                        <svg width="16" height="19" viewBox="0 0 16 19" fill="none" xmlns="http://www.w3.org/2000/svg">
                            <path
                                d="M10.5586 0.841675H5.55859V2.50834H10.5586V0.841675ZM7.22526 11.675H8.89193V6.67501H7.22526V11.675ZM13.9169 6.15834L15.1003 4.97501C14.7419 4.55001 14.3503 4.15001 13.9253 3.80001L12.7419 4.98334C11.4503 3.95001 9.82526 3.33334 8.05859 3.33334C3.91693 3.33334 0.558594 6.69168 0.558594 10.8333C0.558594 14.975 3.90859 18.3333 8.05859 18.3333C12.2086 18.3333 15.5586 14.975 15.5586 10.8333C15.5586 9.07501 14.9419 7.45001 13.9169 6.15834ZM8.05859 16.675C4.83359 16.675 2.22526 14.0667 2.22526 10.8417C2.22526 7.61668 4.83359 5.00834 8.05859 5.00834C11.2836 5.00834 13.8919 7.61668 13.8919 10.8417C13.8919 14.0667 11.2836 16.675 8.05859 16.675Z"
                                fill="white"/>
                        </svg>
                        <p class="pl-2 pb-3">от 30 дней</p>
                    </span>
            </div>
            <div class="part pt-7">
              <p class="pl-3 pr-3 gjol">
                У нас большой опыт ремонта квартир по дизайн проекта. Мы можем разработать для вас авторский проект либо
                сделать ремонт по существующему проекту.
              </p>
              <p class="pl-3 pr-3 gjol">
                Ремонт по проекту как правило сложнее из-за наличия различных декоративных покрытий и элементов (панели,
                декоративная штукатурка, ниши с подсветкой и т.д.).
                В результате занимает больше времени по сроку и стоимости.
              </p>
            </div>
            <div class="lead-btn text-center">
              <Button label="Заказать" severity="secondary"
                      class="price__btn border-noround mt-8 mb-7" outlined/>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
  <section class="steps pt-8 pb-8">
    <div class="container">

      <div class="grid">
        <div class="col-12 md:col-4">
          <h1 class="custom-title">Этапы работы</h1>
        </div>
        <div class="col-12 md:col-8 ">

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
              В ходе беседы с Вами, мы определяем предпочтения, пожелания и увлечения. Фиксируем их в виде
              технического
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
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover pr-2"
                                                       src="https://s3-alpha-sig.figma.com/img/8eb0/d488/aefc56fbccc4c2c3430d8e7e855ae56c?Expires=1697414400&Signature=SYa~EtfMmVS6-8LVN7fW~GTh7ZDQbEXRkvvfXfGIpWmegTnA2llh6TwMFIwKskez7eMN34NIkBNZWpLKga3GvtHRrpfPLMn0M03MZ6-QfWEc2iU4X5KmBAUnlzyXlmJJIJbhxLlal1jDoYAA08NEt~e6XSwvAFfMDI2ppJv6ANtOFkTSllJZ~A0FnVc96129Q1wfXxQh7iFcoGl3N5BRfs5v9hzYvUQelsubmJ0WFoRA50w-CR08Tu6s3ghS3AnfU0qQECKlLqKzzPIj91NJMDKlHHMM2D~lkfU~V49atClvvhMKnp4s7Ba6McZaezF6MFaoypCqGGEMiMXX4AnCiA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                                       alt=""><a href="https://youtu.be/yp5n5DGPrgI"><img class="iht" src="../public/play_button.png" alt=""></a>
            </div>
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover"
                                                       src="https://s3-alpha-sig.figma.com/img/8eb0/d488/aefc56fbccc4c2c3430d8e7e855ae56c?Expires=1697414400&Signature=SYa~EtfMmVS6-8LVN7fW~GTh7ZDQbEXRkvvfXfGIpWmegTnA2llh6TwMFIwKskez7eMN34NIkBNZWpLKga3GvtHRrpfPLMn0M03MZ6-QfWEc2iU4X5KmBAUnlzyXlmJJIJbhxLlal1jDoYAA08NEt~e6XSwvAFfMDI2ppJv6ANtOFkTSllJZ~A0FnVc96129Q1wfXxQh7iFcoGl3N5BRfs5v9hzYvUQelsubmJ0WFoRA50w-CR08Tu6s3ghS3AnfU0qQECKlLqKzzPIj91NJMDKlHHMM2D~lkfU~V49atClvvhMKnp4s7Ba6McZaezF6MFaoypCqGGEMiMXX4AnCiA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                                       alt="">
              <a href="https://youtu.be/yp5n5DGPrgI"><img class="iht" src="../public/play_button.png" alt=""></a>
            </div>
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover pr-2"
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
<style scoped>
.banner__text {
  color: #FFF;

  width: 300px;
  font-size: 13px;
  font-style: normal;
  font-weight: 300;
  line-height: 135%; /* 21.6px */
}
.banner__title {
  color: #FFF;
  font-feature-settings: 'clig' off, 'liga' off;
  font-family: Playfair Display;
  font-size: 42px;
  font-style: normal;
  font-weight: 900;
  line-height: 106.5%; /* 55.38px */
}
.conection{
  background-image: url("http://dom-uyta.ru/img/des.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  height: 100vh;
}
.col-12 {
  padding: 15px;
}

.col-6 {
  padding: 15px;
}

ul li {
  list-style: none;
  padding: 0px;
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






