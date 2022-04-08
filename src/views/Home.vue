<template>
  <section class="fullpage container-fluid section1">
    <div class="home">
      <h1>A Full-Stack Developer</h1>
      <p>I learn how to and make a website, and i love what i do.</p>
    </div>
  </section>
  <section class="colorsection container-fluid">
    <div class="intro">
      <h1 class="reveal">Hello, my name is Benediktus Aprianto</h1>
      <p class="reveal">I've been learning how to code since 2018 and right now focusing on making Websites.</p>
    </div>
  </section>
  <section class="container-fluid reveal section2">
    <div class="skills">
      <template v-for="skill in skills" :key="skill.id">
        <Skillcard 
          :skill = "skill"
        />
      </template>
    </div>
  </section>
  <section class="container-fluid reveal section3">
    <div class="portfolio">
      <h1 class="reveal">Portfolio</h1>
      <p class="reveal">Some of my works</p>
       <div class="card reveal">
        <div class="content">
          <div class="text-content">
            <h2 class="text-white">Sumber Jaya POS System</h2>
            <p class="text-white m-0">a POS System made with Laravel Livewire and Bootstrap for a groceries store called Sumber Jaya</p>
            <p class="text-white m-0 pt-3">Live Website for Public Access Soon...</p>
            <small class="text-muted flex-end">Project is for Private Use</small>
          </div>
          <div class="images">
            <a v-for="(img,index) in sjimages" data-fancybox="Gallery1" :data-src="img.link">
              <img
                v-if="index == 0"
                :src="img.link"
                style="height: 16rem; object-fit: cover; cursor: pointer;"
              >
            </a>
          </div>
        </div>
      </div>
      <div class="card reveal">
        <div class="content">
          <div class="text-content">
            <h2 class="text-white">Photosharing Blog</h2>
            <p class="text-white m-0">Blog System made from scratch using Laravel as a REST API, Vue.JS as the frontend and Bootstrap for CSS Framework</p>
            <p class="text-white m-0 pt-3">Live Website for Public Access Soon...</p>
            <small class="text-muted mb-0 flex-end">Live Website is Only for Private Access</small>
            <small class="text-muted m-0 p-0">Client Only Allow this some screenshot with some blurred information</small>
          </div>
          <div class="images">
            <a v-for="(img,index) in agimages" data-fancybox="Gallery2" :data-src="img.link">
              <img
                v-if="index == 0"
                :src="img.link"
                style="height: 16rem; object-fit: cover; cursor: pointer;"
              >
            </a>
          </div>
        </div>
      </div>
      <div class="card reveal">
        <div class="content">
          <div class="text-content">
            <h2 class="text-white">CV.Kharisma Lestari "Surat Jalan" Making System</h2>
            <p class="text-white m-0">A System to make "Surat Jalan" for items delivery tracking when invoice is not needed</p>
            <p class="text-white m-0">CV.Kharisma Lestari is a Warehouse and shop that sells any kind of deep fried crackers (Kerupuk)</p>
            <p class="text-white m-0 pt-3">Project Still on Progress</p>
            <small class="text-muted flex-end">Project is for Private Use</small>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import LoaderPage from "../components/LoaderPage.vue";
import Skillcard from "../components/Skillcard.vue";
export default {
  name: 'Home',
  components: {
    LoaderPage,
    Skillcard
},
  data() {
    return{
      skills:[
        {
          id:"1",
          svg : '<svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#fff" class="bi bi-laptop" viewBox="0 0 16 16"><path d="M13.5 3a.5.5 0 0 1 .5.5V11H2V3.5a.5.5 0 0 1 .5-.5h11zm-11-1A1.5 1.5 0 0 0 1 3.5V12h14V3.5A1.5 1.5 0 0 0 13.5 2h-11zM0 12.5h16a1.5 1.5 0 0 1-1.5 1.5h-13A1.5 1.5 0 0 1 0 12.5z"/></svg>',
          skillname: 'Front End Development',
          description: "Language and Framework i've been Using:",
          items:[
            {itemname: "Html"},
            {itemname: "Css"},
            {itemname: "JavaScript"},
            {itemname: "Vue 3"},
            {itemname: "Nuxt.js"},
          ]
        },
        {
          id:"2",
          svg : '<svg xmlns="http://www.w3.org/2000/svg" width="40" height="40" fill="#fff" class="bi bi-laptop" viewBox="0 0 16 16"><path d="M13.5 3a.5.5 0 0 1 .5.5V11H2V3.5a.5.5 0 0 1 .5-.5h11zm-11-1A1.5 1.5 0 0 0 1 3.5V12h14V3.5A1.5 1.5 0 0 0 13.5 2h-11zM0 12.5h16a1.5 1.5 0 0 1-1.5 1.5h-13A1.5 1.5 0 0 1 0 12.5z"/></svg>',
          skillname: 'Back End Development',
          description: "Language and Framework i've been Using:",
          items:[
            {itemname: "PHP"},
            {itemname: "Laravel"},
            {itemname: "Laravel Livewire (Fullstack Framework)"},
          ]
        },
      ],
      sjimages:[
        {link:'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjm89Em89ENGrhibq7f3XXGw7GxJ0H_dcUK7n9cQ6_6xxkIaGJJ3EznImE9HkFBkQ2yUkW4mfw20tMhYB0Sy0GyopfI3CgDxFi241FfjfW68rqNtCI_CxJW_8339G1_FnZ3yxIKTqdoPmyYV5w0hIGroLYZ571cr9OEjDaY904zQJ0JDbm7OIooDJyt/s1600/Screenshot_1.png'},
        {link:'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgLtcI1QRGmHOoM-pt0W9WY3OAsa9CkPAR0tvBEnSUG821kCqXntBA-p1lUjrm7smHgEegyBztrIqkC2OVy_YrLG5BOjd37Juz2b5I9BJLvaIuczQDPwYJ7j8hgO8ZvNI_vqd9rWtxoNlT3iO8k_untQiSsKTaT5KZkhqyEfJtFZ0gZLklGMNOpgRxn/s1600/Screenshot_2.png'},
        {link:'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjOkj41TrKiMqdbaREU8RWmdbgv8o5KqdtROLPS-YWe8sIAVFpneV5VZLQQhrZ5NQZQyMihieZg8REXKRUBDa4_yK5Cd9ZoBLwoNXJS-aNDx-Y134WnAtffL7hi-TNb3yZjbrhXkTzmI6Fs6mpjPm6h3GuQc5iJEDpYrmTMCo8nC7ks29dgOj24u-be/s1600/Screenshot_3.png'},
        {link:'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjCL-0ju0qtRagKT_oCVKh4Go-pZHvPXwcERIYmqmnEKgUETs7dez_xUTr8ITp81JY-nxaWHFanZCoG2KpUgHYt4ywvwJ8oEqbq8uomKTb1CZ8wNNRel8t3zDi8pUmAuTngcpDCTlEvPGl1xDtyCcmUZ2G5zS_lZADh_ZDpZYNQv-Fr3S9SFo4VRD9Y/s1600/Screenshot_4.png'},
        {link:'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEhP_3yM-4ToLeWOJkwSiybpCdPTR4YnXsKuloqjgCLjYbIm_AAeWxOHcGbPvLwpbQ2mARS0IDHJK1erunFgvl6ihsdnTc21dyffNtSwC-vU1qbcm4EJE6exHM7GHNxGverNXzWSYek-EwfULZyZCrplADSazQI86Ar4PCgAiaw0XGSKeCWSbNiA1-Kn/s1600/Screenshot_5.png'},
        {link:'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjk3JeRkaxQymwWegJucVtbKsMoN1Y4ygALst0ZuuxF_7R45-7-mQWpwJJhMMcYX7IUFUCXlKMbTPxu1W95VtC6B0hLKeD7En7jT_zNAIV4HTgpqXCA6-DLfQXkPikeT8S7Uad7BG3tg-QLuVMQZomBeOMpa0Ixo9dm2mMrxMLEgfM9_1-v5T4CtfSf/s1600/Screenshot_6.png'},
      ],
      agimages:[
        {link:'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjEbTSsYN1yUvAgR8AAgJgXVADebd8J0Sq5IX6QQ3lunFp5QEDtTquc76K8M_7bkUy-zQYoFo_gW4AuyKUJD0UrM7i-RrOq8VoSqq8dl2--EJ8kRA1FGLkojiHsZaqaLLmXpNcV6RFBBqJ1dEE2NPYkWg1A27yZH2CcheMlG4FIDFovs3z3YWA-aGhZ/s1600/1-blured.jpg'},
        {link:'https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgkZ_Cbl1ay_k2-LSzBzBB9FKvUpeOxHcdfjwUUi96g46j8Qn_pl5P9PlttFz1RT81sXQig13Jo79TqYs4_QKlWlSVTyYB8Af9pRy32lCKCmCbDdxRmqFNR8X7UV0_oMl0FeG6_Zw8a5Q1HiqZhQ1m3MEF263FIdyiGs2nZ7suH8pFrX9mVQyYoRP6J/s1600/2-blured.png'},
      ]
        
      
    }
  },
  beforeCreate: function() {
        document.body.className = 'main';
  },
}

function reveal() {
  var reveals = document.querySelectorAll(".reveal");

  for (var i = 0; i < reveals.length; i++) {
    var windowHeight = window.innerHeight;
    var elementTop = reveals[i].getBoundingClientRect().top;
    var elementVisible = 150;

    if (elementTop < windowHeight - elementVisible) {
      reveals[i].classList.add("active");
    } else {
      reveals[i].classList.remove("active");
    }
  }
}

window.addEventListener("scroll", () => {    
     reveal();    
});

$(function () {
  $(document).scroll(function () {
    var $nav = $(".fixed-top");
    $nav.toggleClass('scrolled', $(this).scrollTop() > $nav.height());
  });
});
</script>
