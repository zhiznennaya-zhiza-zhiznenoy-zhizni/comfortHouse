<script lang="ts" setup>
import {ref} from "vue";
import {Swiper, SwiperSlide} from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';


const items = ref([
  {
    label: 'File',
    icon: 'pi pi-fw pi-file',
    items: [
      {
        label: 'New',
        icon: 'pi pi-fw pi-plus',
        items: [
          {
            label: 'Bookmark',
            icon: 'pi pi-fw pi-bookmark'
          },
          {
            label: 'Video',
            icon: 'pi pi-fw pi-video'
          }
        ]
      },
      {
        label: 'Delete',
        icon: 'pi pi-fw pi-trash'
      },
      {
        separator: true
      },
      {
        label: 'Export',
        icon: 'pi pi-fw pi-external-link'
      }
    ]
  },
  {
    label: 'Edit',
    icon: 'pi pi-fw pi-pencil',
    items: [
      {
        label: 'Left',
        icon: 'pi pi-fw pi-align-left'
      },
      {
        label: 'Right',
        icon: 'pi pi-fw pi-align-right'
      },
      {
        label: 'Center',
        icon: 'pi pi-fw pi-align-center'
      },
      {
        label: 'Justify',
        icon: 'pi pi-fw pi-align-justify'
      }
    ]
  },
  {
    label: 'Users',
    icon: 'pi pi-fw pi-user',
    items: [
      {
        label: 'New',
        icon: 'pi pi-fw pi-user-plus'
      },
      {
        label: 'Delete',
        icon: 'pi pi-fw pi-user-minus'
      },
      {
        label: 'Search',
        icon: 'pi pi-fw pi-users',
        items: [
          {
            label: 'Filter',
            icon: 'pi pi-fw pi-filter',
            items: [
              {
                label: 'Print',
                icon: 'pi pi-fw pi-print'
              }
            ]
          },
          {
            label: 'List',
            icon: 'pi pi-fw pi-bars'
          }
        ]
      }
    ]
  },
  {
    label: 'Events',
    icon: 'pi pi-fw pi-calendar',
    items: [
      {
        label: 'Edit',
        icon: 'pi pi-fw pi-pencil',
        items: [
          {
            label: 'Save',
            icon: 'pi pi-fw pi-calendar-plus'
          },
          {
            label: 'Delete',
            icon: 'pi pi-fw pi-calendar-minus'
          }
        ]
      },
      {
        label: 'Archieve',
        icon: 'pi pi-fw pi-calendar-times',
        items: [
          {
            label: 'Remove',
            icon: 'pi pi-fw pi-calendar-minus'
          }
        ]
      }
    ]
  },
  {
    label: 'Upload',
    icon: 'pi pi-fw pi-upload',
    route: '/fileupload'
  },
  {
    label: 'Quit',
    icon: 'pi pi-fw pi-power-off'
  }
]);
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


  <header class="soedinenie">
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
        <h1 class="banner__title text-white pt-8">Строительство <br>
          уютных коттеджей</h1>
        <p class="banner__text pt-3">Грамотно спроектируем и качественно построим дом Вашей мечты в Екатеринбурге и
          области</p>
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
          <a href="contacts" class="extra__text pt-2 ">контакты</a>
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
            <p class="custom-title pb-6">
              Правильный дом под ключ:
            </p>
          </div>
        </div>
        <div class="grid">
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="68" height="68" viewBox="0 0 68 68" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M67.8501 8.98105L27.4576 0L0.148438 11.3781V22.8028L7.65275 25.1745L0.148438 28.3057V39.7303L4.77119 41.1901L0.148438 43.1154V54.5401L42.7667 68L67.8501 52.033V40.7162L63.7901 39.8086L67.8501 37.2232V25.9065L61.3275 24.453L67.8501 20.2978V8.98105ZM27.8469 4.42177L60.0052 11.5664L40.1178 23.173L8.2938 12.5777L27.8469 4.42177ZM63.6188 49.71L42.1573 63.3667L4.37979 51.4385V45.9377L11.0251 43.1662L42.7603 53.1903L58.7527 43.0138L63.6188 44.1013V49.71ZM63.6188 29.2916V34.896L42.1573 48.5569L4.37979 36.6287V31.128L13.9003 27.1505L42.7603 36.2648L56.2795 27.6604L63.6188 29.2916ZM63.6188 17.9706L42.1573 31.6315L4.37979 19.7033V15.7237L40.5854 27.7937L63.6188 14.3591V17.9706Z"
                    fill="white"/>
                <path d="M17.0741 31.8303H12.8428V36.0617H17.0741V31.8303Z" fill="white"/>
                <path d="M33.9989 38.1775H29.7676V42.4088H33.9989V38.1775Z" fill="white"/>
                <path d="M53.0399 33.946H48.8086V38.1774H53.0399V33.946Z" fill="white"/>
              </svg>

            </div>
            <p class="custom-text">
              Высший класс <br>
              материалов
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
              Фиксированная <br>
              смета
            </p>
          </div>
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="68" height="68" viewBox="0 0 68 68" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0)">
                  <path
                      d="M34 27.5703C25.8711 27.5703 19.2578 34.1836 19.2578 42.3125C19.2578 50.4414 25.8711 57.0547 34 57.0547C42.1289 57.0547 48.7422 50.4414 48.7422 42.3125C48.7422 34.1836 42.1289 27.5703 34 27.5703ZM34 53.0703C28.0681 53.0703 23.2422 48.2443 23.2422 42.3125C23.2422 36.3807 28.0681 31.5547 34 31.5547C39.9319 31.5547 44.7578 36.3807 44.7578 42.3125C44.7578 48.2443 39.9319 53.0703 34 53.0703Z"
                      fill="white"/>
                  <path
                      d="M17 27.5703H10.625C9.52478 27.5703 8.63281 28.4623 8.63281 29.5625C8.63281 30.6627 9.52478 31.5547 10.625 31.5547H17C18.1002 31.5547 18.9922 30.6627 18.9922 29.5625C18.9922 28.4623 18.1002 27.5703 17 27.5703Z"
                      fill="white"/>
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M68.0003 19.5338H48.8249V12H19.1741V19.5338H12.4977H3.5H0V65.1638H12.4977H55.502H68L68.0003 19.5338ZM57.6871 59.2507H62.0872V25.4492H42.9121V17.9154H25.0872V25.4489H5.9131V59.2507H10.3142H57.6871Z"
                        fill="white"/>
                  <path d="M3.5 16.084V19.5338H12.4977V16.084H3.5Z" fill="white"/>
                </g>
                <defs>
                  <clipPath id="clip0">
                    <rect width="68" height="68" fill="white"/>
                  </clipPath>
                </defs>
              </svg>

            </div>
            <p class="custom-text">
              Подробные фотоотчеты <br>
              на этапах строительства
            </p>
          </div>
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="64" height="71" viewBox="0 0 64 71" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M52.6548 1V0.5H52.1548H11.8453H11.3453V1V2.99591C11.3453 7.58441 7.61151 11.318 3.02325 11.318H1.02734H0.527344V11.818V25.091C0.527344 34.7308 3.43158 44.0143 8.92565 51.9353L9.32443 51.6587L8.92565 51.9353C14.4197 59.8561 22.0971 65.8291 31.1257 69.2067L31.8249 69.4683L32.0001 69.5339L32.1753 69.4683L32.8747 69.2067C41.9035 65.8291 49.5809 59.8562 55.0747 51.9353C60.5687 44.0143 63.473 34.7308 63.473 25.091V11.818V11.318H62.973H60.977C56.3885 11.318 52.6548 7.58415 52.6548 2.99591V1ZM58.4813 24.591H58.4811V25.091C58.4811 33.7101 55.8851 42.0079 50.9728 49.0901L51.3836 49.3751L50.9728 49.0901C46.239 55.9152 39.6938 61.1213 32 64.193C24.3064 61.1212 17.761 55.9152 13.0273 49.0901L12.6164 49.3751L13.0273 49.0901C8.11509 42.0081 5.51916 33.7101 5.51916 25.091V16.0752C10.8636 15.0574 15.0848 10.8363 16.1026 5.49181H47.8978C48.9155 10.8363 53.1367 15.0574 58.4813 16.0752V24.591Z"
                    fill="white" stroke="white"/>
                <path
                    d="M20.2713 36.8309L23.094 34.0082L27.6947 38.609L40.9065 25.3971L43.7292 28.2197L27.6947 44.2542L20.2713 36.8309Z"
                    fill="white"/>
              </svg>
            </div>
            <p class="custom-text">
              Пожарная <br>
              безопасность
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
          <img src="http://dom-uyta.ru/img/img6.png" alt="" class="w-full  ">
        </div>
        <div class="col-12 md:col-6 pl-5">
          <div class="desc">
            <p class="custom-title pt-3 ">Полный спектр услуг</p>
            <p class="pb-3 custom-text">
              У нас работает команда специалистов своего дела, которая в любое время готова оказать грамотную
              консультацию и помощь в выборе товаров. Мы поможем вам сделать ремонт и дизайн-проект.
            </p>
            <div class="grid pt-4">
              <div class="col-4">
                <svg width="59" height="59" viewBox="0 0 59 59" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M57.0333 59H1.96667C0.879756 59 0 58.174 0 57.155V47.9387V44.2488V1.84375C0 0.824771 0.879756 0 1.96667 0H27.532H31.4667H57.0333C58.1189 0 59 0.824771 59 1.84375V44.2488V47.9387V57.155C59 58.174 58.1189 59 57.0333 59ZM27.5319 3.68517H5.89989C4.81298 3.68517 3.93322 4.5124 3.93322 5.53261V44.2489H27.5319V3.68517ZM55.0666 5.53261C55.0666 4.5124 54.1855 3.68517 53.0999 3.68517H31.4666V44.2489H55.0666V5.53261ZM55.0666 47.9386H31.4666H27.5319H3.93322V53.4674C3.93322 54.4888 4.81298 55.3123 5.89989 55.3123H53.0999C54.1855 55.3123 55.0666 54.4888 55.0666 53.4674V47.9386ZM39.3327 33.1875H35.4007V22.125H39.3327V33.1875ZM23.6003 33.1875H19.6669V22.125H23.6003V33.1875Z"
                        fill="white"/>
                </svg>
                <p class="pt-2 custom-text"> Эксклюзивный дизайн <br>
                  c 3D визуализацией</p>
              </div>
              <div class="col-4">
                <svg width="57" height="57" viewBox="0 0 57 57" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <g clip-path="url(#clip0)">
                    <path
                        d="M40.5234 19.1552C42.4909 19.1552 44.0859 17.5603 44.0859 15.5928C44.0859 13.6253 42.4909 12.0303 40.5234 12.0303C38.5559 12.0303 36.9609 13.6253 36.9609 15.5928C36.9609 17.5603 38.5559 19.1552 40.5234 19.1552Z"
                        fill="white"/>
                    <path
                        d="M56.385 18.4735C55.196 15.446 53.0158 11.0779 49.3808 7.46018C45.7588 3.85495 41.4369 1.73705 38.4491 0.595048C35.169 -0.658613 31.4416 0.131591 28.9534 2.60808L20.21 11.3106C17.6182 13.8901 16.8712 17.8594 18.351 21.1876C18.8099 22.2198 19.309 23.2294 19.8423 24.2049L0.652158 43.3949C0.234567 43.8125 0 44.3788 0 44.9694V54.7662C0 55.9959 0.996828 56.9928 2.22655 56.9928H12.0234C13.2531 56.9928 14.2499 55.9959 14.2499 54.7662V50.7584L18.2577 50.7583C19.4875 50.7583 20.4843 49.7615 20.4843 48.5317V44.5241H24.4921C25.7218 44.5241 26.7186 43.5272 26.7186 42.2975C26.7186 41.0678 25.7218 40.071 24.4921 40.071H18.2577C17.028 40.071 16.0312 41.0678 16.0312 42.2975V46.3052L12.0234 46.3053C10.7937 46.3053 9.79684 47.3021 9.79684 48.5319V52.5397H4.45311V45.8916L24.1976 26.1472C24.923 25.4218 25.059 24.2948 24.5269 23.4178C23.7553 22.146 23.0465 20.7869 22.4203 19.3783C21.6856 17.726 22.0599 15.7523 23.3517 14.4666L32.095 5.76422C33.3433 4.52191 35.2134 4.12569 36.8596 4.7547C39.4448 5.74284 43.1708 7.56171 46.2396 10.6163C49.3273 13.6894 51.2071 17.4704 52.2402 20.1011C52.8849 21.743 52.4931 23.6083 51.2421 24.8534L42.3931 33.6609C41.1045 34.9433 39.1812 35.3183 37.4929 34.6161C36.1006 34.037 34.752 33.349 33.4851 32.5714C32.4372 31.9281 31.0661 32.2563 30.4229 33.3043C29.7796 34.3524 30.1077 35.7235 31.1557 36.3667C32.6199 37.2654 34.1767 38.0597 35.7827 38.7277C39.1384 40.1236 42.9661 39.3734 45.5345 36.8172L54.3835 28.0097C56.8933 25.5116 57.679 21.7685 56.385 18.4735Z"
                        fill="white"/>
                  </g>
                  <defs>
                    <clipPath id="clip0">
                      <rect width="57" height="57" fill="white"/>
                    </clipPath>
                  </defs>
                </svg>
                <p class="pt-2 custom-text">Ремонт <br> “под ключ”</p>
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

            <p class="f22 custom-text pl-4">Бесплатная разработка <br>
              проекта дома</p>
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
              Гарантия от 5-и лет
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
            <p class="f22 custom-text pl-3">Получим разрешение <br>
              на строительство за вас</p>
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
            <img src="http://dom-uyta.ru/img/catall1.png" class="w-full h677px " alt="">
          </div>
        </div>

      </div>
    </div>
  </section>
  <section class="steps pt-6">
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
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover pr-3"
                                                       src="https://s3-alpha-sig.figma.com/img/8eb0/d488/aefc56fbccc4c2c3430d8e7e855ae56c?Expires=1697414400&Signature=SYa~EtfMmVS6-8LVN7fW~GTh7ZDQbEXRkvvfXfGIpWmegTnA2llh6TwMFIwKskez7eMN34NIkBNZWpLKga3GvtHRrpfPLMn0M03MZ6-QfWEc2iU4X5KmBAUnlzyXlmJJIJbhxLlal1jDoYAA08NEt~e6XSwvAFfMDI2ppJv6ANtOFkTSllJZ~A0FnVc96129Q1wfXxQh7iFcoGl3N5BRfs5v9hzYvUQelsubmJ0WFoRA50w-CR08Tu6s3ghS3AnfU0qQECKlLqKzzPIj91NJMDKlHHMM2D~lkfU~V49atClvvhMKnp4s7Ba6McZaezF6MFaoypCqGGEMiMXX4AnCiA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                                       alt="">
              <a href="https://youtu.be/yp5n5DGPrgI"><img class="iht" src="../public/play_button.png" alt=""></a>
            </div>
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover"
                                                       src="https://s3-alpha-sig.figma.com/img/8eb0/d488/aefc56fbccc4c2c3430d8e7e855ae56c?Expires=1697414400&Signature=SYa~EtfMmVS6-8LVN7fW~GTh7ZDQbEXRkvvfXfGIpWmegTnA2llh6TwMFIwKskez7eMN34NIkBNZWpLKga3GvtHRrpfPLMn0M03MZ6-QfWEc2iU4X5KmBAUnlzyXlmJJIJbhxLlal1jDoYAA08NEt~e6XSwvAFfMDI2ppJv6ANtOFkTSllJZ~A0FnVc96129Q1wfXxQh7iFcoGl3N5BRfs5v9hzYvUQelsubmJ0WFoRA50w-CR08Tu6s3ghS3AnfU0qQECKlLqKzzPIj91NJMDKlHHMM2D~lkfU~V49atClvvhMKnp4s7Ba6McZaezF6MFaoypCqGGEMiMXX4AnCiA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                                       alt="">
              <a href="https://youtu.be/yp5n5DGPrgI"><img class="iht" src="../public/play_button.png" alt=""></a>
            </div>
            <div class="col-12 md:col-6 relative"><img class="w-full h289px object-cover pr-3"
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

.soedinenie {
  background-image: url("http://dom-uyta.ru/img/pexels-max-vakhtbovych-5997993fin.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  height: 100vh;
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






