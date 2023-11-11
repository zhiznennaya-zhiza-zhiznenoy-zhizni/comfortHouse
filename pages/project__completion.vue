<script lang="ts" setup>



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
        <div class=" relative">
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
      <div class="container">
        <h1 class="banner__title text-white pt-8">Подбор материалов <br>
          под ваш бюджет</h1>
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
  <section class="design__project">
    <div class="service-content ">
      <div class="container ">
        <div class="grid pt-3 ">
          <div class="col-12">
            <p class="custom-title pb-8">
              Материалы по выгодным ценам <br>
              в нашем магазине
            </p>
          </div>
        </div>
        <div class="grid flex align-items-center">
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="68" height="68" viewBox="0 0 68 68" fill="none" xmlns="http://www.w3.org/2000/svg">
                <path
                    d="M63.1453 34.1565C62.8283 33.2897 61.8688 32.845 61.0067 33.1631L45.3859 38.8848L58.0129 26.2678C58.3255 25.9567 58.5001 25.5316 58.5001 25.0885C58.5001 24.6471 58.3253 24.2227 58.0129 23.9089L48.2453 14.1359C47.594 13.4846 46.5389 13.4846 45.8876 14.1359L33.5033 26.5115L40.449 10.0354C40.6205 9.62779 40.6228 9.16854 40.4577 8.75931C40.2905 8.35009 39.9682 8.02341 39.56 7.85235L26.8295 2.48443C25.9799 2.12235 25.002 2.52581 24.6448 3.37288L17.7853 19.645V2.31996C17.7853 1.39941 17.0385 0.652588 16.1179 0.652588H1.66737C0.746819 0.652588 0 1.39941 0 2.31996V65.6801C0 66.6007 0.746819 67.3475 1.66737 67.3475H16.1179C16.3215 67.3475 16.5148 67.3051 16.6949 67.239C16.8753 67.3041 17.063 67.3475 17.2583 67.3475C17.45 67.3475 17.6431 67.315 17.832 67.2454L66.9055 49.267C67.7695 48.95 68.2145 47.9926 67.8975 47.1285L63.1453 34.1565ZM9.85664 64.0128H3.33475V61.2622V59.4536V58.2161V53.9249V3.98733H14.4506V27.5551V31.8469V36.1396V45.5525V47.908V50.218V50.2658V60.5957V62.3304V62.8612V62.9545V64.013H14.1492H13.15H9.85664V64.0128ZM36.7289 10.2768L27.2506 32.7604L25.5332 36.8334L23.8154 40.9063L20.8833 47.8611L19.1122 52.061L17.7853 55.2123V52.5474V48.9967V46.9333V44.5755V42.22V28.2301L27.0703 6.20638L36.7289 10.2768ZM23.3932 50.4924L25.1644 46.2927L30.0693 34.6569L47.0644 17.6732L54.4753 25.0874L37.9385 41.6142L32.3285 47.2196L19.2736 60.2655L23.3932 50.4924ZM22.1394 62.1163L39.7749 44.4928L60.5878 36.8681L64.1928 46.7095L22.1394 62.1163Z"
                    fill="white"/>
                <path
                    d="M8.89273 57.1575C8.81944 57.1575 8.75048 57.1737 8.67947 57.1783C8.05472 57.2347 7.50222 57.5224 7.10637 57.964C6.84536 58.2551 6.65268 58.6089 6.55717 59.0019C6.51373 59.1843 6.48389 59.371 6.48389 59.5663C6.48389 60.096 6.65968 60.5801 6.94849 60.9774C7.38633 61.5787 8.09095 61.9739 8.89273 61.9739C9.00924 61.9739 9.1206 61.9566 9.23299 61.9391C9.71386 61.8708 10.1474 61.6623 10.4922 61.3529C10.6587 61.203 10.8057 61.0338 10.9257 60.8426C11.1233 60.5299 11.2437 60.1674 11.2779 59.7787C11.2845 59.7071 11.2991 59.6375 11.2991 59.5649C11.3016 58.2353 10.2231 57.1575 8.89273 57.1575Z"
                    fill="white"/>
              </svg>
            </div>
            <p class="custom-text">
              Ассортимент более <br>
              10000 товаров
            </p>
          </div>
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="82" height="82" viewBox="0 0 82 82" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0)">
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M60.7661 13.7878C61.726 14.4008 62.3894 15.3506 62.6341 16.4628C62.8787 17.5749 62.6752 18.7156 62.0613 19.6749L30.6442 68.7355C30.0113 69.724 29.0347 70.3635 27.9692 70.5979C26.9035 70.8324 25.7489 70.6618 24.7593 70.0299L11.627 61.6464C10.6668 61.0335 10.0034 60.0836 9.75874 58.9714C9.51407 57.8591 9.71759 56.7183 10.3319 55.7591L41.7487 6.69861C43.0146 4.72178 45.6545 4.14081 47.6334 5.40412L60.7661 13.7878ZM56.7874 20.5218L58.7058 17.5261C58.7564 17.4467 58.7539 17.3696 58.7426 17.3189C58.7315 17.2682 58.7015 17.1971 58.622 17.1464L45.4896 8.76273C45.4247 8.72138 45.3491 8.71014 45.2792 8.72552C45.2094 8.74087 45.1455 8.78281 45.1039 8.84756L13.6871 57.9079C13.6362 57.9874 13.6389 58.0644 13.6501 58.1153C13.6612 58.166 13.6911 58.2371 13.7707 58.2878L26.9032 66.6715C27.0331 66.7541 27.2059 66.716 27.2888 66.5868L29.3459 63.3749L31.4945 60.0195L33.5613 56.792L27.6533 52.8888L29.7793 49.6427L35.71 53.4366L37.7767 50.209L39.9253 46.8534L41.9927 43.6263L36.3179 39.8354L38.4617 36.4359L44.1413 40.2708L46.2081 37.0434L48.3567 33.6878L50.4235 30.4603L44.7487 26.6285L46.8925 23.2699L52.5721 27.1048L54.6389 23.8772L56.7874 20.5218Z"
                        fill="white"/>
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M70.3086 26.9845L61.7039 28.9628L62.5599 32.8544L66.4627 31.9104L43.5469 67.6958L43.0615 63.851L39.1702 64.707L40.6878 73.2445C40.9242 74.319 41.987 74.9987 43.0615 74.7623L51.8562 72.5211L51.0002 68.6295L46.9075 69.8364L69.8232 34.0508L70.3086 37.7776L74.2 36.9216L72.6823 28.5021C72.4459 27.4276 71.3832 26.7481 70.3086 26.9845Z"
                        fill="white"/>
                </g>
                <defs>
                  <clipPath id="clip0">
                    <rect width="68" height="68" fill="white" transform="translate(0 14.6089) rotate(-12.406)"/>
                  </clipPath>
                </defs>
              </svg>
            </div>
            <p class="custom-text">
              Выезд на замеры <br>
              и оценка квартиры
            </p>
          </div>
          <div class="col-6 md:col-3">
            <div class="icon pt-3 pb-3">
              <svg width="80" height="80" viewBox="0 0 80 80" fill="none" xmlns="http://www.w3.org/2000/svg">
                <g clip-path="url(#clip0)">
                  <path
                      d="M60.4195 47.563C54.859 47.563 50.3354 52.0866 50.3354 57.647C50.3354 63.2075 54.859 67.7311 60.4195 67.7311C65.9809 67.7311 70.5036 63.2075 70.5036 57.647C70.5036 52.0866 65.98 47.563 60.4195 47.563ZM60.4195 62.6891C57.6389 62.6891 55.3775 60.4277 55.3775 57.647C55.3775 54.8664 57.6389 52.605 60.4195 52.605C63.2001 52.605 65.4615 54.8664 65.4615 57.647C65.4615 60.4278 63.2001 62.6891 60.4195 62.6891Z"
                      fill="white"/>
                  <path
                      d="M25.9659 47.563C20.4054 47.563 15.8818 52.0866 15.8818 57.647C15.8818 63.2075 20.4054 67.7311 25.9659 67.7311C31.5264 67.7311 36.05 63.2075 36.05 57.647C36.05 52.0866 31.5264 47.563 25.9659 47.563ZM25.9659 62.6891C23.1853 62.6891 20.9239 60.4277 20.9239 57.647C20.9239 54.8664 23.1853 52.605 25.9659 52.605C28.7457 52.605 31.0079 54.8664 31.0079 57.647C31.0079 60.4278 28.7465 62.6891 25.9659 62.6891Z"
                      fill="white"/>
                  <path
                      d="M67.211 18.6993C66.7824 17.8481 65.911 17.311 64.958 17.311H51.6807V22.3531H63.4033L70.268 36.0068L74.7739 33.7412L67.211 18.6993Z"
                      fill="white"/>
                  <path d="M52.8569 55.2102H33.7812V60.2522H52.8569V55.2102Z" fill="white"/>
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M9.664 55.2102H18.4034C19.7959 55.2102 20.9245 56.3386 20.9245 57.7311C20.9245 59.1235 19.796 60.2521 18.4035 60.2521H9.664V55.2102Z"
                        fill="white"/>
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M74.512 33.4116L79.4707 39.7982C79.8135 40.2402 80.0001 40.7847 80.0001 41.3444V57.7307C79.9999 59.123 78.8715 60.2516 77.479 60.2516H67.9832C66.5909 60.2516 65.4623 59.1232 65.4623 57.7307C65.4623 56.3383 66.5907 55.2097 67.9832 55.2097H74.9581V42.208L71.2867 37.4786H51.6807C50.2884 37.4786 49.1598 36.3502 49.1598 34.9577V17.3107H9.664V12.2688H51.6809C53.0732 12.2688 54.2018 13.3972 54.2018 14.7897V32.4368H72.5212C73.3002 32.4368 74.0356 32.7965 74.512 33.4116Z"
                        fill="white"/>
                  <path fill-rule="evenodd" clip-rule="evenodd" d="M24.0336 26.988H2.52094V32.0301H24.0336V26.988Z"
                        fill="white"/>
                </g>
                <defs>
                  <clipPath id="clip0">
                    <rect width="80" height="80" fill="white"/>
                  </clipPath>
                </defs>
              </svg>
            </div>
            <p class="custom-text">
              Бесплатная <br>
              доставка на объект
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
              Лучшие цены <br>
              в Екатеринбурге
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="question pt-6 pb-2">
    <div class="container">
      <div class="grid mb-5">
        <div class="col-12 md:col-6">
          <img src="http://dom-uyta.ru/img/magazine_3.png" alt="" class="w-full">
        </div>
        <div class="col-12 md:col-6 pt-6 pl-5">
          <div class="desc">
            <p class="question__title">
              Нет дизайн
              проекта?
            </p>
            <p class="pb-3 question__text">
              Полноценная услуга комплектации интерьера начинается сразу после завершения работ по дизайн-проекту и
              начала
              строительных и ремонтных работ, так как размеры и параметры некоторых позиций напрямую влияют
              на раскладку в чертежах и восприятие эскизов.</p>
            <div class="grid">
              <div class="col">
                <svg width="59" height="59" viewBox="0 0 59 59" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M57.0333 59H1.96667C0.879756 59 0 58.174 0 57.155V47.9387V44.2488V1.84375C0 0.824771 0.879756 0 1.96667 0H27.532H31.4667H57.0333C58.1189 0 59 0.824771 59 1.84375V44.2488V47.9387V57.155C59 58.174 58.1189 59 57.0333 59ZM27.5319 3.68517H5.89989C4.81298 3.68517 3.93322 4.5124 3.93322 5.53261V44.2489H27.5319V3.68517ZM55.0666 5.53261C55.0666 4.5124 54.1855 3.68517 53.0999 3.68517H31.4666V44.2489H55.0666V5.53261ZM55.0666 47.9386H31.4666H27.5319H3.93322V53.4674C3.93322 54.4888 4.81298 55.3123 5.89989 55.3123H53.0999C54.1855 55.3123 55.0666 54.4888 55.0666 53.4674V47.9386ZM39.3327 33.1875H35.4007V22.125H39.3327V33.1875ZM23.6003 33.1875H19.6669V22.125H23.6003V33.1875Z"
                        fill="white"/>
                </svg>


                <p class="custom-text pt-2">
                  Эксклюзивный дизайн <br>
                  c 3D визуализацией
                </p>
              </div>
              <div class="col">
                <svg width="61" height="61" viewBox="0 0 61 61" fill="none" xmlns="http://www.w3.org/2000/svg">
                  <path fill-rule="evenodd" clip-rule="evenodd"
                        d="M60 1.98355C60 2.52641 59.5598 2.96664 59.0165 2.96664H52.1335V18.7002H58.0334C59.1191 18.7011 59.9986 19.5811 60 20.6668V58.0334C59.9986 59.1191 59.1191 59.9986 58.0334 60H4.93327C3.84755 59.9986 2.96799 59.1191 2.96664 58.0334V50.1668H1.98354C1.44023 50.1668 1 49.7266 1 49.1833C1 48.6404 1.44023 48.2002 1.98354 48.2002H7.88345V25.5125L3.93938 29.0749C3.32089 29.6348 2.96754 30.4298 2.96664 31.2643V34.4333C2.96664 34.9766 2.52641 35.4168 1.98354 35.4168C1.44023 35.4168 1 34.9766 1 34.4333V31.2643C1.0009 29.8734 1.59013 28.5478 2.62183 27.6151L30.9659 2.0146C31.6879 1.36101 32.6278 0.999101 33.6019 1H59.0165C59.5598 1 60 1.44023 60 1.98355ZM40.3332 2.96664H33.6019C33.1148 2.96619 32.6453 3.14669 32.2843 3.47349L31.4835 4.19686V28.5334H34.4333C34.9761 28.5329 35.4164 28.0927 35.4168 27.5498V20.6668H34.4333C33.8904 20.6668 33.4502 20.2266 33.4502 19.6833C33.4502 19.1404 33.8904 18.7002 34.4333 18.7002H40.3332V2.96664ZM23.6165 28.5334H25.5832H29.5165V5.97354L20.6668 13.9666V38.3665H23.6165C24.1594 38.3661 24.5996 37.9263 24.6001 37.3835V30.5H23.6165C23.0737 30.5 22.6335 30.0598 22.6335 29.5165C22.6335 28.9736 23.0737 28.5334 23.6165 28.5334ZM18.7002 15.7432L9.85009 23.7363V48.2002H12.7998C13.3427 48.1997 13.7829 47.7595 13.7834 47.2166V40.3332H12.7998C12.257 40.3332 11.8167 39.893 11.8167 39.3501C11.8167 38.8068 12.257 38.3665 12.7998 38.3665H18.7002V15.7432ZM42.2998 18.7002H50.1668V2.96664H42.2998V18.7002ZM49.6195 58.0334H58.0334V20.6655H51.1549L51.1499 20.6668L51.1454 20.6659L41.3181 20.6668H37.3835V27.5498C37.3817 29.1784 36.0619 30.4982 34.4333 30.5H26.5667V37.3835C26.5649 39.012 25.2451 40.3314 23.6165 40.3332H15.75V47.2166C15.7482 48.8452 14.4284 50.165 12.7998 50.1668H4.93327V58.0334H36.9468H49.6195Z"
                        fill="white" stroke="white" stroke-width="2"/>
                </svg>
                <p class="pt-2 custom-text pt-2">
                  Авторский <br>
                  надзор
                </p>
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
  <section class="content01 ">
    <div class="container pb-4">
      <div class="grid">
        <div class="col-12 md:col-4">
          <img src="http://dom-uyta.ru/img/foto-548.png" alt="" class="w-full h-full object-cover">
        </div>
        <div class="col-12 md:col-8 ">
          <p class="custom-title pt-3 pb-2 pl-5">
            Собственный
            выставочный зал
          </p>
          <p class="content__line mt-6 mb-6 "></p>
          <p class="pl-5  custom-text screen">
            Здесь вы сможете посмотреть многие образцы из ассортимента нашего магазина и получить консультацию по
            товару. С нами вы сможете выбрать необходимый материал для вашего ремонта и получить самые выгодные цены!
          </p>
        </div>
        <hr class="mt-5">
      </div>
    </div>
  </section>
  <section class="content02 pb-8x pt-8 ">
    <div class="container">
      <div class="grid">
        <div class="col-12 md:col-3">
          <p class="content02__title">
            Ассортимент <br>
            > 10 000 товаров
          </p>
          <ul>
            <li class="li pl-3 content02__text pt-2">Напольные покрытия</li>
            <li class="li pl-3 content02__text pt-2">Керамическая плитка</li>
            <li class="li pl-3 content02__text pt-2">Настенные покрытия</li>
            <li class="li pl-3 content02__text pt-2">Светильники</li>
            <li class="li pl-3 content02__text pt-2">Сантехника</li>
          </ul>
          <p class="content02__text">посетить онлайн-магазин</p>
        </div>
        <div class="col-12 md:col-9">
          <div class="grid">
            <div class="col-12 md:col-4">
              <img src="http://dom-uyta.ru/img/Group27.png" alt="" class="w-full">
              <p class="content02__text">
                напольные покрытия
              </p>
            </div>
            <div class="col-12 md:col-4">
              <img src="http://dom-uyta.ru/img/Group26.png" alt="" class="w-full">
              <p class="content02__text">
                керамическая плитка
              </p>
            </div>
            <div class="col-12 md:col-4">
              <img src="http://dom-uyta.ru/img/Grou27.png" alt="" class="w-full">
              <p class="content02__text">
                настенные покрытия
              </p>
            </div>
            <div class="col-12 md:col-4">
              <img src="http://dom-uyta.ru/img/Group327.png" alt="" class="w-full">
              <p class="content02__text">
                светильники
              </p>
            </div>
            <div class="col-12 md:col-4">
              <img src="http://dom-uyta.ru/img/Grou23426.png" alt="" class="w-full">
              <p class="content02__text">
                сантехника
              </p>
            </div>
            <div class="col-12 md:col-4">
              <img src="http://dom-uyta.ru/img/Group7527.png" alt="" class="w-full">
              <p class="content02__text">
                мебель для ванны
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <section class="salon pt-6 pb-4">
    <div class="container">
      <h1 class="content02__title">
        Посмотрите наш салон <br>
        в центре Екатеринбурга
      </h1></div>
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
        <div class="col-12 md:col-6 pl-2">
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
  background-image: url("http://dom-uyta.ru/img/foto324234fin.png");
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  width: 100%;
  height: 100vh;
}

.salon {
  background-color: #1e1f25;
  width: 100%;
  height: 100%;
}

.col-4 {
  padding: 15px;
}

.content02__text {
  color: #FFF;
  font-feature-settings: 'clig' off, 'liga' off;

  /* big body */
  font-size: 14px;
  font-style: normal;
  font-weight: 200;
  line-height: 135%; /* 29.7px */
}

.li {
  position: relative;
}

.li:before {
  content: "";
  position: absolute;
  top: 15px;
  left: 0;
  width: 4px;
  height: 4px;
  border-radius: 50%;
  background-color: white;
}

.content02__title {
  color: #FFF;
  font-feature-settings: 'clig' off, 'liga' off;

  /* H1 */
  font-family: Playfair Display;
  font-size: 30px;
  font-style: normal;
  font-weight: 900;
  line-height: 135%; /* 63.45px */
}

.content02 {
  background-color: #353840;
  width: 100%;
  height: 100%;
}

.screen {
  @media screen and (max-width: 768px) {
    padding-top: 100px;
  }
}

.content__line {
  background: white;
  width: 320px;
  height: 0.5px;
  @media screen and (max-width: 768px) {
    display: none;
  }
}

.content01 {
  background-color: #353840;
  width: 100%;
  height: 100%;
}

.question__text {
  color: #FFF;
  font-feature-settings: 'clig' off, 'liga' off; /* Body */
  font-size: 16px;
  font-style: normal;
  font-weight: 300;
  line-height: 135%; /* 21.6px */
}

.question__title {
  color: var(--color-styles-white, #FFF);
  font-feature-settings: 'clig' off, 'liga' off;
  font-size: 38px;
  font-style: normal;
  font-weight: 600;
  line-height: 56px; /* 116.667% */
}

ul {
  padding: 0px;
}


</style>






