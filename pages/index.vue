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


  <header class="header pb-8">
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
    <div class="container ">
      <div class="pl-4 pt-4 " v-if="burger">
        <p class="extra__text  text-white" v-if="burger__extension==false" @click="burger__extension=true">услуги</p>
        <p class="extra__text   text-white" v-if="burger__extension" @click="burger__extension=false">услуги</p>
        <div class="">
          <div class="burger__extension mt-3 mb-3" v-if="burger__extension">
            <p class="">
              <router-link to="interior__design" class="dropdown__items">ДИЗАЙН ИНТЕРЬЕРА</router-link>
            </p>
            <p class="">
              <router-link to="repair__areas" class="dropdown__items   ">РЕМОНТНЫЕ РАБОТЫ</router-link>
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
  <section class="banner pt-7">
    <div class="container relative">

      <img src="http://dom-uyta.ru/img/index.png" class="banner__img" alt="">
      <div class="banner__info flex flex-column align-items-end ">
        <h1 class="banner__title text-right	text-white">Авторский дизайн интерьера и <br> ремонт «под ключ»</h1>
        <p class="banner__text pl300px">Мы - команда полного цикла. Проектируем и реализуем уникальные дизайнерские
          решения в Екатеринбурге.</p>
        <Button label="связаться" severity="secondary" class="btn__text pt-3 pb-3 pl-3 mt-7 "/>
      </div>
    </div>
  </section>
  <section class="benner2">
    <div class="container">
      <h1 class="banner__title text-center	text-white pt-8">Авторский дизайн интерьера и <br> ремонт «под ключ»</h1>
      <p class="banner__text text-center pt-4">Мы - команда полного цикла. Проектируем и реализуем уникальные
        дизайнерские решения в Екатеринбурге.</p>
      <div class="flex justify-content-center">
        <Button label="связаться" severity="secondary" class="btn__text text-center pt-3 pb-3 pl-3 pr-3 mt-7 mb-4 "/>
      </div>
    </div>
  </section>
  <section class="customer ">
    <div class="container">
      <div class="grid pt-8">
        <div class="col-12 sm:col-6">
          <h1 class="text-white customer__title pb-4 pt-6">Мы слышим <br> своих заказчиков</h1>
          <p class="text-white pr-6 pb-8">Для нас важно максимально понять в каком именно пространстве Вам будет
            комфортно жить,
            делаем акцент на стиль и вкус.</p>
          <div class="flex ">
            <div class="">
              <div class="">
                <img src="../public/time.png" alt="">
                <p class="text-white">Соблюдение <br> сроков.</p>
              </div>
            </div>
            <div class="pl50px">
              <div class="">
                <img src="../public/time.png" alt="">
                <p class="text-white">Проектное <br>согласование</p>
              </div>
            </div>
          </div>
        </div>
        <div class="col-12 sm:col-6">
          <img class="w-full h-full object-cover"
               src="https://s3-alpha-sig.figma.com/img/59e7/135b/b0007a75edf5fabbd35c4fa8091b5f47?Expires=1697414400&Signature=jvMZh48JDNWG7z0pXSsBh8gws4MwMiwwLZDIJeROFNOuNfKbnZLFDq0ovisfN-SrxeQcsqb2rwBilvOp4b14f9u0usXufrLv9D3LTaeqnbXCVwbWow5D1cRmZ34pB04cNECXmIy9edVZ65qfjk56lpj9Bjswx5sAVBvx3g~xy9FEMpTmZzC1YaO87EsGgfMRA~xeEIefRkQXNlCgedVIQOGZonlXWKLptOHtMw1GvSWbLtyvtotyz6mbjgJakbLu4cD1BkNrb0O637Hehr3jtMvJelRB28SLGOqNB5nyd~G8opubPPrXjMhrMqJM15bfRyZMErSjVNIkPBr7x5KYfQ__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
               alt="">
        </div>
      </div>
      <div class="grid pt-8 projects pb-8">
        <div class="col-12 md:col-6">
          <div class="grid">
            <div class="col-12 md:col-6"><img class="w-full h-full"
                                              src="https://s3-alpha-sig.figma.com/img/ac5a/9ed8/707b2f62e4e13f5e4bdfbf5edd6660db?Expires=1698019200&Signature=oSEA2fBvbtAFyBQMpSoeEQxh4hrMnvC1-5TdEdUTHokria6uHJM6TkmyOJgy5miZP0PwoVzyRIl4Qe6jfGfeGHXXgbERSEdvv6ORvzJBYz6H66P-jqE9KOGAztkbme06O3vTKlp7RFbgE2i1HNKfbXvw0hdmEJou7lLo8NXeGvEjqtS3eA4R50B5I70pvWl8S-Q1LzysMCmRBG3aoklc3xz1cuk5tA~umZEYbNylwnY2pSCSeud~S2sCLt21GqRHDrFPEK7qCNrHEsBIyR8v8fvvj7Stc56MjMLRi2gqaYnP8MSJnXOHQGF8SG12JM9qcU2pv-7TI~65Wf0s02pw9g__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                              alt=""></div>
            <div class="col-12 md:col-6"><img class="w-full h-full object-cover"
                                              src="https://s3-alpha-sig.figma.com/img/9e8c/1325/16e560ff2d8e0fc59118ded56f1c3f20?Expires=1698019200&Signature=lTe3AXb6MfiTS8hcHSZKgohetI-eRSWSC-uBnyvsK5-NPYG-CDjuFCeMENc78PMWMFG1uPfaVCN7EOXwzCLGa1C7~rzA-TMvLny1ki5ClIAigqkDkGquieCk0j2mPNLDXCDjGZxKwg3ZKniZ2akb8VN2LEiCzyLl8ZfvLWF-vesNP5Dpe1lcT57JrCIxc6BjdnPeXJUDz8Ghl3WQ1~dhkePzN1NDeTZxytNSDywa4WwlhrpHYIiXxXTPlH~9-hmd8zQdG~HSHr5XAMo7rKDPqxwp1va75SAtCQhli7AN-Udi-o7CyVStIqxqKy9vT4-w~bZmkTQTR9WXOH850peCZw__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"
                                              alt=""></div>
          </div>
        </div>
        <div class="col-12 md:col-6 projects__block pl-6">
          <h1 class="projects__title text-white pt-5">Комплектуем проекты</h1>
          <p class="projects__subtitle text-white pb-4">На этапе проектирования Вы сможете посмотреть отделочные
            материалы в нашем
            салоне в живую. При реализации
            проекта мы закупим и доставим все материалы, а вам не придется ездить по множеству магазинов.</p>
          <div class="flex ">
            <div class="">
              <div class="">
                <img src="../public/time.png" alt="">
                <p class="text-white">Соблюдение <br> сроков.</p>
              </div>
            </div>
            <div class="pl50px">
              <div class="">
                <img src="../public/time.png" alt="">
                <p class="text-white">Проектное <br>согласование</p>
              </div>
            </div>
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
          <img class="w-full h-full object-cover" src="https://dom-uyta.ru/img/lamp.png" alt="">
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


.benner2 {
  display: none;

  @media screen and (max-width: 1041px) {
    display: block;
    background-image: url("http://dom-uyta.ru/img/index.png");
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

.banner__text {
  color: #FFF;

  /* Body */
  font-size: 13px;
  font-style: normal;
  font-weight: 300;
  line-height: 135%; /* 21.6px */
}

.banner__info {
  position: absolute;
  top: 30px;
  left: 400px;
}

.banner__title {
  font-family: "Playfair Display", serif;
  font-weight: 900;
  font-size: 42px;
}

.banner {
  background-color: #23242a;
  width: 100%;
  height: 100%;
  @media screen and (max-width: 1041px) {
    display: none;
  }
}

.banner__img {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  width: 630px;
  height: 380px;
}

.col-12 {
  padding: 7px;
}

.burger__extension {
  display: block;
  padding: 0.25rem 1rem;
  clear: both;
  font-weight: 400;
  color: black;
  text-align: inherit;
  text-decoration: none;
  white-space: nowrap;
  background-color: #3d3e45;
  border: 0;
  padding-top: 10px;
  padding-bottom: 10px;
}

.extra__text {
  color: #FFF;
  font-feature-settings: 'clig' off, 'liga' off;

  /* Small H */
  font-family: Gilroy;
  font-size: 12px;
  font-style: normal;
  font-weight: 999;
  line-height: normal;
  letter-spacing: 1.5px;
  text-transform: uppercase;
}

.dropdown__items {
  padding-left: 20px;
  padding-top: 5px;
  font-weight: 999;
  font-size: 12px;
  line-height: 15px;
  letter-spacing: 1.5px;
  text-transform: uppercase;
  color: #999999;

}

.dropdown__item {
  display: block;
  width: 320px;
  height: 150px;
  padding: 0.25rem 1rem;
  clear: both;
  font-weight: 400;
  color: black;
  text-align: inherit;
  text-decoration: none;
  white-space: nowrap;
  background-color: #3d3e45;
  border: 0;
  padding-top: 10px;
  padding-bottom: 10px;
  position: absolute;
  left: 100px;
  top: 60px;
}

.questions {
  background-color: #24252b;
}

ul li {
  list-style: none;
  padding: 0px;
}


</style>






