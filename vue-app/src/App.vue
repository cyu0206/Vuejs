<script setup>
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-icons/font/bootstrap-icons.css'
import 'bootstrap/dist/js/bootstrap.js'

import BindingComponent from './components/BindingComponent.vue';
import BMIComponent from './components/BMIComponent.vue';
import ComputedDemo from './components/ComputedDemo.vue';
import FirstComponent from './components/FirstComponent.vue';
import MyComponent from './components/MyComponent.vue';

import SecondComponent from './components/SecondComponent.vue';
import WatchDemo from './components/WatchDemo.vue';
import AboutView from './views/AboutView.vue';
import ContactView from './views/ContactView.vue';
import HomeView from './views/HomeView.vue';
import NavbarComponent from './components/NavbarComponent.vue';
import DirectiveComponent from './components/DirectiveComponent.vue';
import EventModifiers from './components/EventModifiers.vue';



</script>

<template>
    <div class="container">
        <!-- <h2>Hello Vue!!!!!</h2> -->
        <NavbarComponent></NavbarComponent>
        <!-- <RouterLink to="/">首頁</RouterLink> | 
 <RouterLink to="/about">關於我們</RouterLink> | 
 <RouterLink to="/contact">聯絡我們</RouterLink> |  -->

        <hr />
        <!--是一個容器，根據路由，載入不同的Component-->
        <RouterView></RouterView>

        <hr />
        <div>
            <!-- <DirectiveComponent></DirectiveComponent>
     <EventModifiers></EventModifiers> -->
            <img class="img1" src="/images/loading.gif" alt="loading" />
        </div>



        <!-- <HomeView></HomeView>
 <AboutView></AboutView>
 <ContactView></ContactView>
 
  <BMIComponent></BMIComponent>
<WatchDemo></WatchDemo>
 <ComputedDemo></ComputedDemo>

 <MyComponent></MyComponent>
 <FirstComponent></FirstComponent>
<SecondComponent></SecondComponent>  
<BindingComponent></BindingComponent>-->

    </div>


</template>

<style scoped>
h2 {
    color: green
}

.img1 {
    /* scaleX(-1) rotate(180deg); */
    transform: translateX(0px) rotate(0deg);
    opacity: 1;
}

.img1:hover {
    transform: translateX(300px) rotate(360deg);
    opacity: 0;

    transition: all 3s;
}
</style>
