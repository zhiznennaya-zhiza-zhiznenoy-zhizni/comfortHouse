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
  <!--  <header>-->
  <!--    <div class="container">-->
  <!--      <div class="grid">-->
  <!--        <nav class="navbar navbar-expand-lg">-->
  <!--          <div class="container-fluid">-->
  <!--            <a class="navbar-brand" href="/">-->
  <!--              <img src="/img/logo.png" class="img-fluid descktop-logo" alt="">-->
  <!--              <img src="/img/logo-wbg.png" class="img-fluid mobile-logo" alt="">-->
  <!--            </a>-->
  <!--            <a href="tel:+73432885813" class="mobile-phone mgo-number" id="call_tel">+7 (343) 288-58-13</a>-->
  <!--            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">-->
  <!--              <svg width="21" height="14" viewBox="0 0 21 14" fill="none" xmlns="http://www.w3.org/2000/svg">-->
  <!--                <rect width="21" height="2" fill="#3B3B3B" />-->
  <!--                <rect y="6" width="21" height="2" fill="#3B3B3B" />-->
  <!--                <rect y="12" width="21" height="2" fill="#3B3B3B" />-->
  <!--              </svg>-->
  <!--            </button>-->
  <!--            <div class="collapse navbar-collapse" id="navbarSupportedContent">-->
  <!--              <ul class="navbar-nav me-auto mb-2 mb-lg-0">-->
  <!--                <li class="nav-item dropdown">-->
  <!--                  <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false">-->
  <!--                    услуги-->
  <!--                  </a>-->
  <!--                  <ul class="dropdown-menu" aria-labelledby="navbarDropdown">-->
  <!--                    <li><a class="dropdown-item" href="/design/">дизайн интерьера</a></li>-->
  <!--                    <li><a class="dropdown-item" href="/remont/">ремонтные работы</a></li>-->
  <!--                    <li><a class="dropdown-item" href="/cottages/">строительство коттеджей</a></li>-->
  <!--                    <li><a class="dropdown-item" href="/equipment/">комплектация проектов</a></li>-->
  <!--                  </ul>-->
  <!--                </li>-->
  <!--                <li class="nav-item">-->
  <!--                  <a class="nav-link" href="/portfolio/">портфолио</a>-->
  <!--                </li>-->
  <!--                <li class="nav-item">-->
  <!--                  <a class="nav-link" href="/about/">о нас</a>-->
  <!--                </li>-->
  <!--                <li class="nav-item">-->
  <!--                  <a class="nav-link" href="#contacts">контакты</a>-->
  <!--                </li>-->
  <!--              </ul>-->
  <!--              <div class="d-flex">-->
  <!--                <a href="tel:+73432885813" class="desc-phone mgo-number" id="call_tel">+7 (343) 288-58-13</a>-->
  <!--                <a href="https://www.instagram.com/dom_uyta_ekb/" target="_blank">-->
  <!--                  <svg width="29" fill="white" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512">-->
  <!--                    &lt;!&ndash;! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. &ndash;&gt;-->
  <!--                    <path d="M224.1 141c-63.6 0-114.9 51.3-114.9 114.9s51.3 114.9 114.9 114.9S339 319.5 339 255.9 287.7 141 224.1 141zm0 189.6c-41.1 0-74.7-33.5-74.7-74.7s33.5-74.7 74.7-74.7 74.7 33.5 74.7 74.7-33.6 74.7-74.7 74.7zm146.4-194.3c0 14.9-12 26.8-26.8 26.8-14.9 0-26.8-12-26.8-26.8s12-26.8 26.8-26.8 26.8 12 26.8 26.8zm76.1 27.2c-1.7-35.9-9.9-67.7-36.2-93.9-26.2-26.2-58-34.4-93.9-36.2-37-2.1-147.9-2.1-184.9 0-35.8 1.7-67.6 9.9-93.9 36.1s-34.4 58-36.2 93.9c-2.1 37-2.1 147.9 0 184.9 1.7 35.9 9.9 67.7 36.2 93.9s58 34.4 93.9 36.2c37 2.1 147.9 2.1 184.9 0 35.9-1.7 67.7-9.9 93.9-36.2 26.2-26.2 34.4-58 36.2-93.9 2.1-37 2.1-147.8 0-184.8zM398.8 388c-7.8 19.6-22.9 34.7-42.6 42.6-29.5 11.7-99.5 9-132.1 9s-102.7 2.6-132.1-9c-19.6-7.8-34.7-22.9-42.6-42.6-11.7-29.5-9-99.5-9-132.1s-2.6-102.7 9-132.1c7.8-19.6 22.9-34.7 42.6-42.6 29.5-11.7 99.5-9 132.1-9s102.7-2.6 132.1 9c19.6 7.8 34.7 22.9 42.6 42.6 11.7 29.5 9 99.5 9 132.1s2.7 102.7-9 132.1z" />-->
  <!--                  </svg>-->
  <!--                </a>-->
  <!--                <a class="btn btn-outline-warning form-modal" data-bs-toggle="modal" data-bs-target="#form" data-from="header-menu">связаться</a>-->
  <!--              </div>-->
  <!--            </div>-->
  <!--          </div>-->
  <!--        </nav>-->
  <!--      </div>-->
  <!--    </div>-->
  <!--  </header>-->
  <!--  <section class="Our__services">-->
  <!--    <div class="container">-->
  <!--      <h1 class="services__title text-white">Наши услуги</h1>-->
  <!--      <div class="grid">-->
  <!--        <div class="md:col-6 lg:col-3 " style="margin-bottom: 70px">-->
  <!--          <div class="services__block">-->
  <!--            <img-->
  <!--                src="https://s3-alpha-sig.figma.com/img/f6fd/3279/b86c33f4eb4d8bea6f51bbf8f6e0a2af?Expires=1697414400&Signature=ZHl~S0MD6pQP9apWOPEtEwPF2lTHVM81ymu4fqlyCqTrigyQO~W~1aA0ZyVtuCU9CELT8D0rpPE~eTD0AC1-WbJTCVHjE6MLBjzXreXGfvhOpwbmnKki4lb28vDG9-FeILH~6U8JCI8eqTiFsBz8uWWq9avdaDif9-F4uMJfSuAUswJIsj~dIOMFjLltpFXCDK5mkFBKzZL5UdKbFMWBEhZv9NWX4sJQE6qKVDGyFtWpQLOJbe7ahjEe1YvF5AD7LVbQU7wS76pxNt0iGU1Fu3n~~Q4o5gk-RacBiB9Q2lr8XAY5nM2nsUXOqKgKxHXzVP~dyKIjI75NjfDwVA8ogA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"-->
  <!--                alt="">-->
  <!--            <p class="services__subtitle">Дизайн <br>интерьера</p>-->
  <!--          </div>-->
  <!--        </div>-->
  <!--        <div class="md:col-6 lg:col-3">-->
  <!--          <div class="services__block">-->
  <!--            <img-->
  <!--                src="https://s3-alpha-sig.figma.com/img/6f4c/17ec/fa87c940440de890ee45951a5382dde5?Expires=1697414400&Signature=jiXQtK29uGMqTxVzcOn7ABhX9nlaAwN-YG7PqsTGSpq18Ap9jIgaFE-HzqbAJVgn0SnPyGOYSK~HK0FaFnTaMVhGqEAw6Qv1JcSu5wWS4k4I4oVq-9JDnSCZ86BsqPCGD2kON4K~FeFg7fFZaJLf67GMBA2OoY2jylijAbUHelUSsJK0Kwa-G-vd5KdNjuZxtYhA8JHjYTU5~dyu0YLyMysa1UdeRihdLhHCnmkO9dhhVU6wdFnng4wIL~CP0iQ1xUnGWGDsO3KXWKyw2fN5atr-x-O7wlCbD3vcC7lf20DsQPjy4BOlVlG10Pi4TDTOM8ZilmmlxqmVTS7kfT9Bjw__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"-->
  <!--                alt="">-->
  <!--            <p class="services__subtitle">Ремонт <br>квартир и домов</p>-->
  <!--          </div>-->
  <!--        </div>-->
  <!--        <div class="md:col-6 lg:col-3">-->
  <!--          <div class="services__block">-->
  <!--            <img-->
  <!--                src="https://s3-alpha-sig.figma.com/img/f6fd/3279/b86c33f4eb4d8bea6f51bbf8f6e0a2af?Expires=1697414400&Signature=ZHl~S0MD6pQP9apWOPEtEwPF2lTHVM81ymu4fqlyCqTrigyQO~W~1aA0ZyVtuCU9CELT8D0rpPE~eTD0AC1-WbJTCVHjE6MLBjzXreXGfvhOpwbmnKki4lb28vDG9-FeILH~6U8JCI8eqTiFsBz8uWWq9avdaDif9-F4uMJfSuAUswJIsj~dIOMFjLltpFXCDK5mkFBKzZL5UdKbFMWBEhZv9NWX4sJQE6qKVDGyFtWpQLOJbe7ahjEe1YvF5AD7LVbQU7wS76pxNt0iGU1Fu3n~~Q4o5gk-RacBiB9Q2lr8XAY5nM2nsUXOqKgKxHXzVP~dyKIjI75NjfDwVA8ogA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"-->
  <!--                alt="">-->
  <!--            <p class="services__subtitle">Строительство <br>коттеджей</p>-->
  <!--          </div>-->
  <!--        </div>-->
  <!--        <div class="md:col-6 lg:col-3">-->
  <!--          <div class="services__block">-->
  <!--            <img-->
  <!--                src="https://s3-alpha-sig.figma.com/img/f6fd/3279/b86c33f4eb4d8bea6f51bbf8f6e0a2af?Expires=1697414400&Signature=ZHl~S0MD6pQP9apWOPEtEwPF2lTHVM81ymu4fqlyCqTrigyQO~W~1aA0ZyVtuCU9CELT8D0rpPE~eTD0AC1-WbJTCVHjE6MLBjzXreXGfvhOpwbmnKki4lb28vDG9-FeILH~6U8JCI8eqTiFsBz8uWWq9avdaDif9-F4uMJfSuAUswJIsj~dIOMFjLltpFXCDK5mkFBKzZL5UdKbFMWBEhZv9NWX4sJQE6qKVDGyFtWpQLOJbe7ahjEe1YvF5AD7LVbQU7wS76pxNt0iGU1Fu3n~~Q4o5gk-RacBiB9Q2lr8XAY5nM2nsUXOqKgKxHXzVP~dyKIjI75NjfDwVA8ogA__&Key-Pair-Id=APKAQ4GOSFWCVNEHN3O4"-->
  <!--                alt="">-->
  <!--            <p class="services__subtitle">Комплектация <br>проектов</p>-->
  <!--          </div>-->
  <!--        </div>-->
  <!--      </div>-->
  <!--    </div>-->
  <!--  </section>-->
  <header class="header">
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
    <div class="container">
      <div class="pl-4 pt-4" v-if="burger">
        <p class="extra__text  text-white" v-if="burger__extension==false" @click="burger__extension=true">услуги</p>
        <p class="extra__text   text-white" v-if="burger__extension" @click="burger__extension=false">услуги</p>
        <div class="">
          <div class="burger__extension mt-3 mb-3" v-if="burger__extension">
            <p class=""> <router-link to="interior__design" class="dropdown__items">ДИЗАЙН ИНТЕРЬЕРА</router-link></p>
            <p class=""> <router-link to="repair__areas" class="dropdown__items">РЕМОНТНЫЕ РАБОТЫ</router-link></p>
            <p class=""> <router-link to="construction__cottages" class="dropdown__items">СТРОИТЕЛЬСТВО КОТТЕДЖЕЙ</router-link></p>
            <p class=""> <router-link to="project__completion" class="dropdown__items">КОМПЛЕКТАЦИЯ ПРОЕКТОВ</router-link></p>

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
  <section class="our__works">
    <div class="container pt-5 pb-5">
      <div class="grid align-items-center">
        <div class="col-12 sm:col-6">
          <div class="flex justify-content-between align-items-center">
            <h1 class="our__works__title">Наши работы</h1>
            <img src="public/filter%201.png" class="h20px our__works__filter" alt="">
          </div>
        </div>
        <div class="col-12 sm:col-6">
          <div class="grid justify-content-between">
            <span>
              <router-link to="" class="our__works__menu__text text-white">Все</router-link>
            </span>
            <span>
              <router-link to="" class="our__works__menu__text text-white">Дизайн</router-link>
            </span>
            <span>
              <router-link to="" class="our__works__menu__text text-white">Ремонт</router-link>
            </span>
            <span>
              <router-link to="" class="our__works__menu__text text-white">Коттеджи</router-link>
            </span>
            <span>
              <router-link to="" class="our__works__menu__text text-white">видеообзоры</router-link>
            </span>
          </div>
        </div>
      </div>
      <div class="settings pb-4">
        <Button label="1-комнатные" class="border-noround border-gray color-gray remut1  bg-transparent"
                severity="secondary"/>
        <Button label="2-комнатные" class="border-noround border-gray color-gray remut   bg-transparent"
                severity="secondary"/>
        <Button label="3-комнатные" class="border-noround border-gray color-gray remut  bg-transparent"
                severity="secondary"/>
        <Button label="4+ комнатные" class="border-noround border-gray color-gray remut mt-3  bg-transparent"
                severity="secondary"/>
        <Button label="дома" class="border-noround border-gray color-gray remut mt-3  bg-transparent"
                severity="secondary"/>
        <Button label="студии" class="border-noround border-gray color-gray remut mt-3  bg-transparent"
                severity="secondary"/>
      </div>
    </div>
  </section>
  <section class="video">
    <div class="container pb-8">
      <div class="grid">
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/8e0/1000_750_2/8e02b54ebfe9daeb63f167beb8caef21.jpg"
              alt=""
              class="w-full images ">
          <div class="text-overlay z-10">
            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/6cf/1000_750_2/6cf91c5cd5086483c2825a840a4385f6.jpeg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">
            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/2fb/1000_750_2/2fb0252998c2693e974bb4d53211528f.jpg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">

            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/c48/1000_750_2/c48a43a1658e9e15d9ebb63ed05e012c.jpg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">

            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/062/1000_750_2/0623dcfc3a7b4a9223baaaf6c2cbbc18.jpeg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">

            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/545/1000_750_2/545d9dda560ea496482d09200be508a4.jpeg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">

            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
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
    <div class="container pb-8 pt-8">
      <div class="grid">
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/8e0/1000_750_2/8e02b54ebfe9daeb63f167beb8caef21.jpg"
              alt=""
              class="w-full images ">
          <div class="text-overlay z-10">
            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/6cf/1000_750_2/6cf91c5cd5086483c2825a840a4385f6.jpeg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">
            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/2fb/1000_750_2/2fb0252998c2693e974bb4d53211528f.jpg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">

            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/c48/1000_750_2/c48a43a1658e9e15d9ebb63ed05e012c.jpg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">

            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/062/1000_750_2/0623dcfc3a7b4a9223baaaf6c2cbbc18.jpeg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">

            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
          </div>
        </div>
        <div class="col-12 md:col-6 posit">
          <img
              src="https://dom-uyta.ru/upload/resize_cache/iblock/545/1000_750_2/545d9dda560ea496482d09200be508a4.jpeg"
              alt=""
              class="w-full images ">
          <div class="text-overlay">

            <p class="text-white center__text">Дизайн интерьера
              в 3-к квартире</p>
            <p class="see">
              <router-link to="" class="see">СМОТРЕТЬ</router-link>
            </p>
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
  <section class="questions ">
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
  <section class="contacts" id="contacts">
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
            <div class="col-12 lg:col-4 ">
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
<style >
ul li {
  list-style: none;
  padding: 0px;
}

</style>






