<template>
  <div class="first">
    <section class="image-group6">
      <div class="contact-info">
        <p class="contact-us">Contact us</p>
        <a href="mailto: info@vedras.hr">info@vedras.hr</a>
        <a class="phone-number" href="tel:385989608920">+385 98 9608 920</a>
        <span class="language-switch"><NuxtLink to="/">HR</NuxtLink></span>
      </div>
      <div class="contact-info-response">
        <a href="mailto: info@vedras.hr">info@vedras.hr</a>
        <a class="phone-number-response" href="tel:385989608920">+385 98 9608 920</a>
        <span class="language-switch-response"><NuxtLink to="/">HR</NuxtLink></span>
      </div>
      <img class="image-group4" src="~assets/images/Group4.svg" alt="slika4">
      <hr class="line">
      <h1 class="on-hold">ON HOLD</h1>
      <div class="social">
        <a style="" href="https://www.instagram.com/vedrasgroup/?hl=en"><font-awesome-icon class="
          font-awesome" :icon="['fab', 'instagram']" style="color:white; font-size: 18px;"/></a>
        <a href="https://www.facebook.com/vedrasevents/"><font-awesome-icon class="
          font-awesome" :icon="['fab', 'facebook']" style="color:white; font-size: 18px;"/></a>
        <a href="https://www.linkedin.com/company/42940956/"><font-awesome-icon class="
          font-awesome" :icon="['fab', 'linkedin']" style="color:white; font-size: 18px;"/></a>
      </div>
    </section>

    <section class="row section2">
      <div class="section2-div1">
        <p class="section2-paragraf1">In the midst of the current situation with Co-vid19, our “event” industry is completely stopped. 
          It is really hard to predict the start of big gatherings and coffee parties that are close 
          to the summer we are used to. Despite the temporary pause of the entire event industry, 
          Vedras does not want to stand aside and wait for this pandemic to end on its own, 
          but as we always do, we are embarking on new ventures and victories. This time around, we are introducing something completely new, 
          something unrelated to our usual business. 
          We present something that will help us combat this pandemic and make everyone return to normal as soon as possible.
        </p>
        <img class="robots-logo" src="~assets/images/UVD-Robots-logo-tagline-black-website.png">
        <img class="boston-medical-logo" src="~assets/images/boston-medical-logo-color-jpg.png">
        <p class="section2-paragraf2">We want to inform you of the availability of a 
          new autonomous UV disinfection robot from the Blue Ocean Robotics company.</p>
      </div>
      <div class="section2-div2">
        <div>
          <img class="kill-stroj" src="~assets/images/kill-stroj.png">
        </div>
        <div>
          <div class="mikroorganizmi slow">
            <p>KILLS 99,99% OF MICROORGANISMS</p>
          </div>
        </div>
      </div>
    </section>

    <section class="row section3">
      <div class="novo-u-ponudi">
        <h3 class="section3-header">New in our offer!</h3>
        <p class="section3-paragraf1">Secure robot disinfection and sterilization with applications in: </p>
        <ul class="section3-ul">
          <li class="section3-list"> Tourism (hotels, apartments, holiday homes, mobile homes ...)</li>
          <li class="section3-list"> Industry (factories, warehouses, plants ...)</li>
          <li class="section3-list"> Public places (health centers, kindergartens, schools, colleges, 
            offices, airports, stations, fitness gyms, shopping centers ...)</li>
        </ul>
        <p class="section3-paragraf2">Robots designed to clean operating rooms and laboratories 
          are now disinfecting your business and private spaces.</p>
        <a class="detalji-uvd-robots" href="ttp://www.uvd-robots.com/">More details about UVD Robots</a>
      </div>
      <div class="offer slow"></div>
    </section>

    <section class="row section4">
      <div class="holding-tablet-uvd-robots slow"></div>
      <div class="section4-covidfree reveal">
        <h3 class="section4-hashtag">#covidfree</h3>
        <p class="section4-paragraf1">By applying ultraviolet light (UV, UV-c), the UVD robot destroys the structure of DNA in all microorganisms.</p>
        <p class="section4-paragraf2">With help of robots, we provide a service for cleaning large and small spaces, 
          which in the shortest possible time and autonomously disinfect indoors where safety 
          and “sense of cleanliness” must come first.</p>
      </div>
    </section>

    <section class="row section5">
      <div class="image-group7"></div>
      <div class="cist-prostor">
        <p class="section5-paragraf1">You want to provide a secure place to stay or work for your costumers or employees. 
          Search no more and contact us now. Let your spaces be #covidfree
        </p>
      </div>
    </section>

    <section class="row section6">
      <div class="section6-nase-osoblje slow">
        <h3 class="section6-header">Our staff is ready to provide a service as soon as possible which includes: </h3>
        <ul class="section6-ul">
          <li class="section6-list">delivery of UV disinfection robot</li>
          <li class="section6-list">mapping of the rooms intended for disinfection</li>
          <li class="section6-list">control of operation during disinfection</li>
          <li class="section6-list">collection of the UV disinfection robot</li>
        </ul>
        <a class="brosura" href="http://vedras.hr/download/Vedras_dezinfekcija_UVD_Robotima.pdf"><button class="preuzmi-brosuru">DOWNLOAD BROCHURE</button></a>
      </div>
      <div class="image-bolnicka-soba reveal"></div>
    </section>

    <section class="section7-fotter">
      <p class="section7-paragraf1">Contact us for more: </p>
      <div class="section7-mail-mob">
        <span class="slower"><a class="section7-mail" href="mailto:info@vedras.hr">info@vedras.hr</a></span>
        <span class="slower"><p class="section7-paragraf2">or call us</p></span>
        <span class="slow"><a class="section7-mob" href="tel:385989608920">+385 98 9608 920</a></span>
      </div>
    </section>        
  </div> 
</template>
  
<script>
  
  export default {
  created(){
    window.addEventListener('scroll', reveal);

  function reveal(){
    var reveals = document.querySelectorAll('.reveal');
    

    for(var i=0; i<reveals.length; i++){
      var windowheight = window.innerHeight;
      var revealtop = reveals[i].getBoundingClientRect().top;
      var revealpoint = 80;

      if(revealtop<windowheight-revealpoint){
        reveals[i].classList.add('active');
      }
      else{
        reveals[i].classList.remove('active');
      }
    }
  }
  window.addEventListener('scroll', slow);

  function slow(){
    var reveals = document.querySelectorAll('.slow');

    for(var i=0; i<reveals.length; i++){
      var windowheight = window.innerHeight;
      var revealtop = reveals[i].getBoundingClientRect().top;
      var revealpoint = 50;

      if(revealtop<windowheight-revealpoint){
        reveals[i].classList.add('active');
      }
      else{
        reveals[i].classList.remove('active');
      }
    }
  }
  window.addEventListener('scroll', slower);

  function slower(){
    var reveals = document.querySelectorAll('.slower');

    for(var i=0; i<reveals.length; i++){
      var windowheight = window.innerHeight;
      var revealtop = reveals[i].getBoundingClientRect().top;
      var revealpoint = 80;

      if(revealtop<windowheight-revealpoint){
        reveals[i].classList.add('active');
      }
      else{
        reveals[i].classList.remove('active');
      }
    }
  }
  }
}
  
</script>
  
<style scoped>

.first{
  font-family: 'Titillium Web', sans-serif;
}
.image-group6{
  background-image: url("~assets/images/Group6.jpg");
  height: 347px;
  background-position-x: 50%;
}
.contact-info {
  padding: 30px 13.125vw 7px 13.125px; 
  letter-spacing: -.29px;
  text-align: right;
}
.contact-info-response{
  display: none;
}
.contact-us{
  margin:0;
  font-weight: 700;
  display: inline-block;
  color: white;
  line-height: 32px;
  font-size: 16px;
}
a{
  color: white;
  padding-left: 8px;
  padding-right: 8px;
  letter-spacing: -.29px;
  text-decoration: none;
  line-height: 32px;
  font-size: 16px;
}
a:hover{
  color: #d8d2d2;
  text-decoration: underline;
}
.phone-number{
  padding-right: 35px;
  padding-left: 0;
}
.language-switch{
  font-weight: 700;
}
.image-group4{
  display: block; 
  max-width: 100%;
  height: auto; 
  margin: auto;
}
.line{  
  background-color: #fff;
  width: 437px;
  border: 1px solid #fff;
  margin-top: 30px;
  margin-bottom: 30px;
}
.on-hold{
  color: white; 
  font-size: 36px;
  font-weight: 700;
  line-height: 48px;
  letter-spacing: -.64px;
  text-align: center;
  animation:transitionIn 2s;
}
@keyframes transitionIn {
  from{
    opacity: 0;
    transform:translateY(10%)
  }
  to{
    opacity: 1;
    transform:translateY(0)
  }
}
.social{
  text-align: center;
}
.social a{
  padding: 5px;
}
.font-awesome:hover{
  color: #d8d2d2 !important;
}
.row{
  width: 100%;
  display:flex;
}
.section2{
  padding: 80px 13.125vw 80px 13.125vw;
}
.section2-div1{
  width: 51%;
  animation:transitionIn1 2s;
}
@keyframes transitionIn1 {
  from{
    opacity: 0;
    transform:translateY(10%)
  }
  to{
    opacity: 1;
    transform:translateY(0)
  }
}
.section2-paragraf1{
  padding-bottom: 30px;
  color: #5c5c5c;
  font-size: 16px;
  letter-spacing: -.29px;
  margin:0;
}
.robots-logo{
  height: 161px;
  width: 303.42px;
  margin-bottom: 30px;
  display: block;
  max-width: 100%;
}
.boston-medical-logo{
  height: 64px;
  width: 366.81px;
  display: block;
  max-width: 100%;
}
.section2-paragraf2{
  width: 342px;
  padding-top: 30px;
  color: #5c5c5c;
  font-size: 16px;
  letter-spacing: -.29px;
  margin:0;
}
.section2-div2{ 
  width: 42%;
  margin-left: 7%; 
  position: relative;
}
.kill-stroj{
  z-index: 5;
  margin-top: -40px;
  display: block;
  max-width: 100%;
  position: relative;
  animation:transitionIn2 1s;
}
@keyframes transitionIn2 {
  from{
    opacity: 0;
  }
  to{
    opacity: 1;
  }
}
.mikroorganizmi{
  background-color: #027FC1;
  height: 170px;
  width: 350px;
  font-size: 24px;
  font-weight: 700;
  letter-spacing: -.43px;
  line-height: 36px;
  margin-top: -110px;
}
.mikroorganizmi p{
  color: white;
  padding-top: 40px;
  padding-left: 30px;
  padding-right: 30px;
}
.section3{
  padding-top: 80px;
  padding-bottom:80px;
  background-color: #027fc1;
  margin:0
}
.novo-u-ponudi{
  width: 40%;
  padding: 0px 80px 0px 13.125vw; 
}
.section3-header{
  color: white;
  margin: 0;
  font-size: 36px;
  font-weight: 700;
  line-height: 48px;
  padding-bottom: 30px;
  padding-top: 70px;
  letter-spacing: -.64px;
}
.section3-paragraf1{
  margin: 0;
  color: white;
  font-size: 16px;
  letter-spacing: -.29px;
  line-height: 32px;
}
.section3-ul{
  padding-left: 20px;
}
.section3-list{
  font-weight: 700;
  color:white;
  font-size: 16px;
  letter-spacing: -.29px;
  line-height: 32px;
}
.section3-paragraf2{
  margin: 0;
  padding-top: 26px;
  padding-bottom: 26px;
  color: white;
  font-size: 16px;
  letter-spacing: -.29px;
  line-height: 32px;
}
.detalji-uvd-robots{
  font-weight: 700;
  color: white;
  font-size: 16px;
  letter-spacing: -.29px;
  line-height: 32px;
  padding: 0;
}
.offer{
  width: 50%;
  background-image: url("~assets/images/offer.png");
  background-size: cover;
  background-position-x: 50%;
  height: 574px;
  width: 42.96vw;
  margin-left: 220px;
}
.section4{
  margin:0;
  padding: 160px 10vw 160px 10vw;
}
.holding-tablet-uvd-robots{
  background-image: url("~assets/images/holding-tablet-uvd-robots.jpg");
  background-size: cover;
  height: 464px;
  width: 49%;
  margin-right: 1%;
}
.section4-covidfree{
  height: 464px;
  width:49%;
  margin-left:1%;
  box-shadow: 0 2px 32px 0 rgb(0 0 0 / 14%);
  padding: 100px 70px 100px 70px;
}
.section4-hashtag{
  color: #5c5c5c;
  font-size: 36px;
  font-weight: 700;
  letter-spacing: -.64px;
  line-height: 48px;
  margin: 0;
  padding: 0;
}
.section4-paragraf1{
  color: #5c5c5c;
  font-size: 16px;
  letter-spacing: -.29px;
  margin: 0;
  padding: 30px 0px 30px 0px;
}
.section4-paragraf2{
  color: #5c5c5c;
  font-size: 16px;
  letter-spacing: -.29px;
  margin: 0;
  padding: 0;
}
.section5{
  margin: 0;
  padding:0;
}
.image-group7{
  background-image: url("~assets/images/Group7.jpg");
  background-size: cover;
  background-position-x: 0%;
  height: 631px;
  width: 50%;
  margin: 0;
  padding: 0;
}
.cist-prostor{
  width: 50%;
  background-color: #027fc1;
  margin: 0;
  padding: 200px 50px 190px 50px;
}
.section5-paragraf1{
  color: white;
  font-size: 36px;
  font-weight: 700;
  letter-spacing: -.64px;
  line-height: 55px;
  padding-left: 50px;
  padding-right: 50px; 
}
.section6{
  margin:0;
  padding: 120px 13.125vw 120px 13.125vw;
}
.section6-nase-osoblje{
  box-shadow: 0 2px 32px 0 rgb(0 0 0 / 14%);
  width: 53%;
  height: 600px;
  margin-right: 1%; 
  padding: 105px 50px 105px 50px; 
}
.section6-header{
  color: #5c5c5c;
  font-size: 36px;
  font-weight: 700;
  letter-spacing: -.64px;
  line-height: 50px;
  margin: 0;
  padding: 0;
}
.section6-ul{
  padding: 30px 0px 50px 20px;
  margin: 0;
}
.section6-list{
  color: #5c5c5c;
  font-size: 16px;
  letter-spacing: -.29px;
  margin: 0;
  padding: 0;
}
.image-bolnicka-soba{
  background-image: url("~assets/images/bolnicka-soba.jpg");
  background-size: cover;
  background-position-y: 80%;
  height: 600px;
  width: 42%;
  margin-left: 4%;
}
.brosura{
  padding-left: 0;
}
.preuzmi-brosuru{
  background-color: #027fc1;
  color: white;
  width: 11.5vw;
  height: 3vw;
  border: none;
  letter-spacing: -.29px;
}
button:hover{
  background-color: white;
  color: #027fc1;
  border: 1px solid #027fc1;
  transition: all 0.15s ease-in-out;
  transition-property: all;
  transition-duration: 0.15s;
  transition-delay: 0s;
  transition-timing-function: ease-in-out;
}
.section7-fotter{
  background-color: #027fc1;
  margin: 0;
  padding-top: 120px;
  padding-bottom: 120px;
  letter-spacing: -.29px;
}
.section7-paragraf1{
  margin: 0;
  color: white;
  font-size: 36px;
  text-align: center;
  line-height: 48px;
}
.section7-mail-mob{
  margin: 0;
  text-align: center;
}
.section7-mail-mob a{
  padding: 0;
  display:inline-block;
  font-weight: 700;
  font-size: 36px;
  line-height: 48px;
}
.section7-mail-mob a:hover{
  color: #d8d2d2;
  text-decoration: underline;
}
.section7-paragraf2{
  display:inline-block;
  font-size: 36px;
  line-height: 48px;
  color: white;
  margin: 0;
  padding-left: 7px;
  padding-right: 7px;
}
.reveal{
  position: relative;
  transform: translateY(80px);
  opacity: 0;
  transition: all 2s ease;
}
.reveal.active{
  transform: translateY(0px);
  opacity: 1;
}
.slow{
  opacity: 0;
  transition: all 2s ease;
}
.slow.active{
  opacity: 1;
}
.slower{
  opacity: 0;
  transition: all 4s ease;
}
.slower.active{
  opacity: 1;
}

@media(max-width: 1600px){
  .contact-info {
    padding-left: 9.5vw;
    padding-right: 9.5vw;
  }
  .contact-info-response{
    display: none;
  }
  .section2 {
    padding-left: 10.8vw;
    padding-right: 10.8vw;
  }
  .section2-div2 {
    width: 47.5%;
    margin-left: 1.5%;
  }
  .novo-u-ponudi {
    padding-left: 10vw;
  }
  .offer {
    margin-left: 155px;
  }
  .cist-prostor {
    padding-top: 205px;
    padding-bottom: 130px;
  }
  .section6-nase-osoblje {
    width: 49%;
    margin-right: 5%;
    padding-top: 75px;
    padding-bottom: 75px;
    height: 535px;
  }
  .section6 {
    padding-left: 10vw;
    padding-right: 10vw;
  }
  .preuzmi-brosuru {
    width: 14vw;
    height: 3.5vw;
  }
  .image-bolnicka-soba {
    height: 535px;
    width: 38%;
    margin-left: 8%;
  }

}
@media(max-width: 1550px){
  .contact-info-response{
  display: none;
  }
  .section3-header{
    padding-top: 85px;
  }
  .offer{
    margin-left:170px;
  }
  .image-group7{
    background-position-x: 100%;
  }
}
@media(max-width: 1450px){
  .contact-info-response{
  display: none;
  }
  .section2-div1{
    width: 49%;
  }
  .section2-div2{
    width:49.5%;
  }
  .cist-prostor{
    padding-top: 150px;
    padding-bottom: 130px;
  }
  .preuzmi-brosuru{
    width: 14.7vw;
    height: 4vw;
  }
  .section6-nase-osoblje{
    height: 575px;
  }
  .image-bolnicka-soba{
    height: 575px;
  }

}
@media(max-width: 1350px){
  .contact-info-response{
  display: none;
  }
  .section2-div1{
    width: 48%;
  }
  .section2-div2{
    width: 50.5%;
  }
  .kill-stroj{
    max-width: 105%;
    margin-top: 0px;
  }
  .section3{
    padding-top: 85px;
  }
  .section3-header{
    padding-top: 42px;
  }
  .offer{
    margin-left: 140px;
  }
  .holding-tablet-uvd-robots{
    width: 46.5%;
  }
  .section4-covidfree{
    width: 51.5%;
  }
  .cist-prostor{
    padding-top: 155px;
    padding-bottom: 130px;
  }
  .preuzmi-brosuru{
    width: 16vw;
    height: 4.5vw;
  }
  .image-bolnicka-soba{
    background-position-x: 50%;
  }
}
@media(max-width: 1250px){
  .contact-info-response{
  display: none;
  }
  .section2{
    padding-left: 11vw;
    padding-right: 11vw;
  }
  .section2-div1{
    width: 46.5%;
  }
  .section2-div2{
    width: 52%;
  }
  .kill-stroj{
    margin-top: 10px;
  }
  .mikroorganizmi{
    margin-top: -95px;
  }
  .novo-u-ponudi{
    padding-left: 10.2vw;
  }
  .section3-header{
    padding-top: 22px; 
  }
  .section3-paragraf2{
    padding-top: 15px;
  }
  .offer{
    margin-left: 125px;
  }
  .holding-tablet-uvd-robots{
    width: 45.5%;
  }
  .section4-covidfree{
    width: 52.5%;
  }
  .cist-prostor{
    padding-top: 120px;
    padding-bottom: 100px;
  }
  .preuzmi-brosuru{
    width: 17.7vw;
    height: 5vw;
  }
}
@media(max-width: 1150px){
  .contact-info-response{
  display: none;
  }
  .section2{
    padding-left: 11.5vw;
    padding-right: 11.5vw;
  }
  .section2-div1{
    width: 44%;
  }
  .section2-div2{
    width: 52%;
    margin-left: 1%;
  }
  .kill-stroj{
    margin-top: 40px;
    max-width: 115%;
  }
  .mikroorganizmi{
    margin-top: -68px;
    margin-left: 30px;
    width: 340px;
  }
  .novo-u-ponudi{
    padding-left: 11.3vw;
  }
  .offer{
    margin-left: 110px;
  }
  .holding-tablet-uvd-robots{
    width: 45%;
  }
  .section4-covidfree{
    width: 52.5%;
    padding-right: 80px;
    padding-left: 80px;
    padding-top: 90px;
    padding-bottom: 90px;
  }
  .cist-prostor{
    padding-top: 75px;
    padding-bottom: 40px;
  }
  .image-bolnicka-soba{
    height: 560px;
  }
  .section6-nase-osoblje {
      padding-top: 35px;
      padding-bottom: 35px;
      height: 560px;
  }
}
@media(max-width: 1050px){
  .contact-info-response{
  display: none;
  }
  .section2-div1{
    width: 43.9%;
  }
  .section2-div2{
    width: 52%;
    margin-left: 1%;
  }
  .kill-stroj{
    margin-top: 70px;
  }
  .mikroorganizmi p{
    padding-top: 47px;
  }
  .section3{
    padding-top: 60px;
  }
  .novo-u-ponudi{
    width: 90%;
    padding-right: 0;
    padding-left: 10.7vw;
  }
  .offer{
    background-size: cover;
    background-position-y: 70%;
    width: 80%;
    margin-top: 50px;
    margin-right: 0;
    height: 36.2vh;
    min-height: 300px;
  }
  .section4{
    flex-direction: column-reverse;
  }
  .holding-tablet-uvd-robots{
    width: 100%;
    margin: 0;
    height: 42.96vh;
    min-height: 300px;
    background-position-y: 100%;
  }
  .section4-covidfree{
    width: 100%;
    height: auto;
    margin: 0;
    margin-bottom: 7%;
    padding-top: 50px;
    padding-bottom: 50px;
    padding-left: 70px;
    padding-right: 70px;
  }
  .section5{
    flex-direction: column-reverse;
  }
  .image-group7{
    width: 100%;
    height: 50vh;
    min-height: 300px;
  }
  .cist-prostor{
    padding-bottom: 30px;
    padding-top: 30px;
    width: 100%;
  }
  .section6-nase-osoblje{
    width: 100%;
    height: 460px;
    margin: 0;
    margin-bottom: 7%;
  }
  .preuzmi-brosuru{
    width: 23vw;
    height: 5.8vw;
  }
  .image-bolnicka-soba{
    width: 50%;
    height: 460px;
    margin-left: 25%;
  }

}
@media(max-width: 950px){
  .contact-info-response{
  display: none;
  }
  .section2-div1{
    width: 47.5%;
  }
  .section2-div2{
    width: 51%;
    margin-left: 1.5%;
  }
  .kill-stroj{
    margin-top: 100px;
    max-width: 105%;
  }
  .novo-u-ponudi{
    padding-left: 10vw;
    width: 88%;
  }
  .offer{
    margin-left: 10%;
  }
  .section4-covidfree{
    padding-right: 100px;
    padding-left: 70px;
  }
  .cist-prostor{
    padding-bottom: 35px;
    padding-top: 45px;
  }
  .section6-nase-osoblje{
    height: 460px;
  }
  .preuzmi-brosuru{
    width: 23vw;
    height: 6vw;
  }

}
@media(max-width: 850px){
  .contact-info-response{
  display: none;
  }
  .section2{
    padding-right: 8.5vw;
    padding-left: 11.7vw;
  }
  .section2-div1{
    width: 100%;
  }
  .section2-paragraf2{
    width: 100%;
  }
  .section2-div2{
    width: 100%;
    margin: 2%;
  }
  .kill-stroj{
    margin-top: 25px;
  }
  .mikroorganizmi{
    margin-left: 0;
    width: 100%;
  }
  .mikroorganizmi p{
    margin-bottom: 0;
    text-align: center;
  }
  .preuzmi-brosuru{
    width: 27vw;
    height: 7vw;
  }
  .image-bolnicka-soba{
    height: 420px;
  }
  .section7-mail-mob{
    padding-right: 30%;
    padding-left: 30%;
  }
}
@media(max-width: 750px){
  .contact-info-response{
  display: none;
  }
  .contact-info{
    padding-right: 1.5vw;
  }
  .image-group4{
    margin-top: 25px;
  }
  .line{
    width: 85%;
  }
  .section2{
    margin: 0;
    padding-right: 3vw;
    padding-left: 3vw;
  }
  .section2-div2{
    margin: 0;
    width: 100%;
    margin-left: 5%;
  }
  .mikroorganizmi{
    width: 95%;
  }
  .novo-u-ponudi{
    width: 100%;
    padding-left: 3vw;
    padding-right: 3vw;
  }
  .section3-header{
    font-size: 25px;
  }
  .section3-list{
    line-height: 25px;
  }
  .section3-paragraf2{
    line-height: 25px;
    padding-top: 20px;
    padding-bottom: 20px;
  }
  .offer{
    width: 96%;
    margin-right: 2.9%;
    margin-left: 2.9%;
  }
  .section4{
    padding-right: 3vw;
    padding-left: 3vw;
  }
  .section4-covidfree{
    padding-left: 70px;
    padding-right: 70px;
  }
  .section4-hashtag{
    font-size: 25px;
  }
  .cist-prostor{
    font-size: 25px;
    padding-bottom: 45px;
  }
  .section5-paragraf1{
    line-height: 32px;
    margin: 0;
    padding-left: 0;
    padding-right: 0;
    font-size: 25px;
  }
  .image-group7{
    height: 55vh;
  }
  .section6{
    padding-right: 3vw;
    padding-left: 3vw;
  }
  .section6-nase-osoblje{
    height: 370px;
    padding-bottom: 0;
    padding-left: 3vw;
    padding-right: 3vw;
  }
  .section6-header{
    line-height: 32px;
    font-size: 25px;
  }
  .preuzmi-brosuru{
    width: 31vw;
    height: 8vw;
  }
  .image-bolnicka-soba{
    background-position-y: 70%;
    margin: 0;
    height: 420px;
    width: 100%;
  }
  .section7-paragraf1{
    font-size: 25px;
    line-height: 32px;
  }
  .section7-mail-mob a{
    font-size: 25px;
    line-height: 32px;
  }
  .section7-paragraf2{
    line-height: 32px;
    font-size: 25px;
  }
}
@media(max-width: 650px){
  .contact-info{
    display: none;
  }
  .contact-info-response{
    padding-top: 30px;
    padding-bottom: 7px;
    text-align: right; 
    padding-left: 13.125vw;
    padding-right: 10px; 
    letter-spacing: -.29px;
    display:block;
  }
  .contact-us-response{
  margin:0;
  font-weight: 700;
  display: inline-block;
  color: white;
  line-height: 32px;
  font-size: 16px;
}
.phone-number-response{
  padding-right: 20px;
  padding-left: 0;
}
.language-switch-response{
  font-weight: 700;
}
.section2{
  padding-top: 30px;
  padding-bottom: 30px;
}
.section2-div2{
  margin-left: 0;
}
.kill-stroj{
  max-width: 100%;
}
.mikroorganizmi{
    width: 100%;
  }
.section3{
  padding-top: 20px;
  padding-bottom: 20px;
}
.section4{
  padding-bottom: 40px;
  padding-top: 40px;
}
.section4-covidfree{
  padding-left: 25px;
  padding-right: 25px;
}
.section6{
  padding-top: 40px;
  padding-bottom: 40px;
}
.preuzmi-brosuru{
  height: 9vw;
  width: 35vw;
}
.section7-fotter{
  padding-top: 40px;
  padding-bottom: 40px;
}
}
@media(max-width: 550px){
  .section2{
    padding-left: 3.5vw;
    padding-right: 3.5vw;
  }
  .novo-u-ponudi{
    padding-left: 3.5vw;
    padding-right: 3.5vw;
  }
  .section4{
    padding-left: 3.5vw;
    padding-right: 3.5vw;
  }
  .section6{
    padding-left: 3.5vw;
    padding-right: 3.5vw;
  }
  .section6-nase-osoblje{
    height: 400px;
  }
  .preuzmi-brosuru{
    width: 42vw;
    height: 11vw;
  }
}
@media(max-width: 450px){
  a{
    font-size: 13px;
  }
  .section2{
    padding-left: 4vw;
    padding-right: 4vw;
  }
  .mikroorganizmi p{
    text-align: left;
  }
  .section3{
    padding-top: 10px;
    padding-bottom: 10px;
  }
  .novo-u-ponudi{
    padding-left: 4.5vw;
    padding-right: 5vw;
  }
  .offer{
    margin-bottom: 4%;
    margin-left: 5%;
    margin-right: 5%;
  }
  .section4{
    padding-right: 4vw;
  }
  .section4-covidfree{
    margin-bottom: 13%;
    padding-bottom: 30px;
  }
  .section6{
    padding-right: 4.5vw;
    padding-left: 4.5vw;
  }
  .section6-nase-osoblje{
    margin-bottom: 13%;
    height: 420px;
  }
  .section6-nase-osoblje a{
    font-size: 16px;
  }
  .preuzmi-brosuru{
    height: 13vw;
    width: 53vw;
  }
  .section7-fotter{
    padding-left: 20px;
    padding-right: 20px;
  }
  .section7-mail-mob{
    padding-right: 20%;
    padding-left: 20%;
  }
}
@media(max-width: 350px){
  .section2{
    padding-left: 5vw;
    padding-right: 5vw;
  }
  .mikroorganizmi{
    width: 100%;
    margin-left: 0;
  }
  .section4{
    padding-left: 8vw;
    padding-right: 8vw;
  }
  .section4-covidfree{
    padding-left: 15px;
    padding-right: 15px;
  }
  .section6{
    padding-left: 6vw;
    padding-right: 6vw;
  }
  .section6-nase-osoblje{
    height: 540px;
    padding-left: 7vw;
    padding-right: 7vw;
    margin-bottom: 15%;
  }
  .preuzmi-brosuru{
    height: 18vw;
    width: 65vw;
  }
  .section7-mail-mob{
    padding-left: 10%;
    padding-right: 10%;
  }
}
</style>