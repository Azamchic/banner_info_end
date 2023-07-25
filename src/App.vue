<template>
  <header class="header">
    <div class="navbar">
      <div class="logo rounded-md"><a href="#">CAR MUSIC</a></div>
      <ul class="links">
        <li><a href="hero">HOME</a></li>
        <li><a href="about">ABOUT</a></li>
        <li><a href="services">SERVICES</a></li>
        <li><a href="contact">CONTACT</a></li>
      </ul>
      <a href="#" class="action_btn">Get Started</a>
      <div class="toggle_btn w-[20px] h-[10px]" :onclick="toggleMenu">
        <i class="fa-solid fa-bars text-3xl"></i>
      </div>
    </div>
    <div class="dropdown_menu" v-if="isActive">
      <li><a href="hero">HOME</a></li>
        <li><a href="about">ABOUT</a></li>
        <li><a href="services">SERVICES</a></li>
        <li><a href="contact">CONTACT</a></li>
        <li><a href="#" class="action_btn">Get Started</a></li>
    </div>
    
    <div class="text_logo">
      <h1 class="text">CAR MUSIC</h1>
      <p class="layout" >Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vitae orci urna amet penatibus.</p>
      <button class="btn">Наши услуги</button>
    </div>

    <div class="container">
      <div class="left">
        <div class="box">
          <h1 class="text">адрес:</h1>
          <h2 class="layout">Lorem ipsum dolor sit amet, consectetur adipiscing elit </h2>
        </div>
      </div>
      <div class="center">
        <div class="box">
          <h1 class="text">телефон:</h1>
          <h2 class="tel1">8 (812) 123-45-67</h2>
          <h2 class="tel2">8-911-123-45-67</h2>
        </div>
      </div>
      <div class="right">
        <div class="box">
          <h1 class="text">Режим работы:</h1>
          <h2 class="job1">пн-пт : 10:00 - 20:00</h2>
          <h2 class="job2">сб-вск : 12:00 - 20:00</h2>
        </div>
      </div>
    </div>

  </header>

  <div class="banner">
    <div class="left">
      <div class="container">
        <div class="wrapper">
          <div class="image_text">
            <img src="./assets/image/Group 53.png" alt="logo">
            <h1 class="text">материалы от лучших компаний</h1>
          </div>
          <p class="title">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pretium, rutrum est, molestie proin tristique duis sed. Morbi suspendisse amet nisl vestibulum risus. Quis pretium</p>
        </div>

        <div class="wrapper mb-[50px]">
          <div class="image_text">
            <img class="img2" src="./assets/image/Group 52.png" alt="logo">
            <h1 class="text">Опытные мастера</h1>
          </div>
          <p class="title">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Et donec elementum egestas vitae ullamcorper. Amet volutpat ornare pharetra amet adipiscing orci, lectus aenean ultricies. Erat viverra eget blandit ornare. Molestie ipsum commodo faucibus rhoncus</p>
        </div>

        <div class="wrapper">
          <div class="image_text">
            <img  src="./assets/image/Group 54.png" alt="logo">
            <h1 class="text">Гарантия на все виды работы</h1>
          </div>
          <p class="title">Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vestibulum volutpat.</p>
        </div>
      </div>
    </div>
    <div class="right"></div>
  </div>

  



  
</template>

<script>
export default {
  data(){
    return{
      isActive: false
    }
  },

  methods: {
    toggleMenu() {
    this.isActive = !this.isActive
}
    }
  }



</script>

<style>


  li{
    list-style: none;
  }

  a{
    text-decoration: none;
    color: #000;
    font-size: 30px;
  }
  a:hover{
    color: red;
    transition: 1s;
  }

  header{
    position: relative;
    padding: 0 2rem;
  }
  .navbar{
    width: 100%;
    height: 60px;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .navbar .logo a{
    font-size: 40px;
    font-weight: bold;
    color: red;
  }

  .navbar .links{
    display: flex;
    gap: 2rem;
    color: #fff;
    font-weight: 500;
  }

  .navbar .toggle_btn{
    color: red;
    font-size: 1.5rem;
    cursor: pointer;
    display: none;
  }

  .action_btn{
    background-color: red;
    color: green;
    padding: 0.5rem 1rem;
    border: none;
    outline: none;
    border-radius: 20px;
    font-size: 0.8rem;
    font-weight: bold;
    cursor: pointer;
    width: 140px; 
    height: 50px;
    font-size: 20px;
  }

  .action_btn:hover{
    scale: 1.05;
    color: #fff ;
  }

  .action_btn{
    scale: 0.95;
  }

  /* dropdown */
  .dropdown_menu{
    display: none;
    position: absolute;
    right: 2rem;
    top: 60px;
    height: 0;
    width: 300px;
    background: rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(15px);
    border-radius: 10px;
    overflow: hidden;
    transition: 0.5s;
    color: red;
    
  }

  .dropdown_menu{
    height: 280px;

  }

  .dropdown_menu li{
    padding: 0.7rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .dropdown_menu .action_btn{
    width: 100%;
    display: flex;
    justify-content: center;
  }

  .header{
    width: 100%;
    height: 900px;
    background: url(./assets/image/car_music.png) no-repeat center / cover;
    margin: 0 auto;
  }

    .header .text_logo{
      width: 500px;
      margin: 0 auto;
    }

    .header .text_logo .layout{
      color: #fff;
      width: 400px;
      height: 97px;
      font-weight: 500;
      text-align: center;
      font-size: 24px;
      margin: 0 0 0 30px;
    }

    .header .text_logo .text{
      font-size: 90px;
      color: red;
      font-weight: 500;
      margin-top: 200px;
      margin-left: 20px;
    }

    .header .text_logo .btn{
      color: #fff;
      background: red;
      width: 110px;
      height: 61px;
      border: 2px solid red;
      cursor: pointer;
      margin: 30px 0 0 169px;
    }

    .header .container{
      display: flex;
      max-width: 150%;
      height: 220px;
      margin: 80px auto;
      gap: 20px;
    }

    .header .container .left{
      width: 50%;
      border: 1px solid #fff;
      height: 220px;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }

    .header .container .left .box{
      width: 265px;
      height: 115px;
    }

    .header .container .left .box .text{
      width: 45px;
      height: 25px;
      font-size: 18px;
      font-weight: 500;
      margin: 0 auto;
      color: #fff;
    }

    .header .container .left .box .layout{
      width: 265px;
      height: 70px;
      margin: 0 auto;
      font-size: 20px;
      font-weight: 600;
      text-align: center;
      color: red;
    }

    .header .container .center{
      width: 50%;
      border: 1px solid #fff;
      height: 220px;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }

    .header .container .center .box{
      width: 144px;
      height: 128px;
    }

    .header .container .center .text{
      font-size: 18px;
      font-weight: 600;
      color: #fff;
      margin: 0 0 0 35px;
    }

    .header .container .center .tel1{
      color: red;
      width: 160px;
      height: 34px;
      font-size: 20px;
      font-weight: 600;
      margin: 0 auto;
      cursor: pointer;
    }

    .header .container .center .tel2{
      color: red;
      width: 160px;
      height: 34px;
      font-size: 20px;
      font-weight: 600;
      margin: 0 0 0 5px;
      cursor: pointer;
    }
    
    .header .container .right{
      width: 50%;
      height: 220px;
    }

    .header .container .right{
      width: 50%;
      border: 1px solid #fff;
      height: 220px;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
    }

    .header .container .right .box{
      width: 190px;
      height: 130px;
    }

    .header .container .right .text{
      color: #fff;
      font-size: 20px;
      font-weight: 600;
      margin: 0 0 0 20px;
    }

    .header .container .right .job1{
      color: red;
      width: 200px;
      height: 35px;
      font-size: 20px;
      font-weight: 600;
    }

    .header .container .right .job2{
      color: red;
      width: 200px;
      height: 35px;
      font-size: 20px;
      font-weight: 600;
    }

    .banner{
      width: 100%;
      height: 700px;
      background: #000;
      display: flex;
    }

    .banner .left{
      width: 50%;
      height: 660px;
      
    }

    .banner .left .container{
      width: 100%;
      height: 660px;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      gap: 20px;
    }

    .banner .left .container .wrapper{
      width: 526px;
      height: 160;
      
    }

    .banner .left .container .wrapper .image_text{
      width: 526px;
      height: 160px;
      display: flex;
      justify-content: space-around;
      align-items: center;
    }

    .banner .left .container .wrapper .image_text .img2{
      width: 70px;
      height: 45px;
      
    }


    .banner .left .container .wrapper .image_text img{
      width: 56px;
      height: 70px;
    }

    .banner .left .container .wrapper .image_text .text{
      width: 426px;
      height: 43px;
      font-size: 27px;
      font-weight: 600;
      color: #fff;
    }
    
    .banner .left .container .wrapper .title{
      width: 526px;
      height: 58px;
      font-size: 18px;
      font-weight: 500;
      margin-top: -20px;
      color: #fff;
    }

    .banner .right{
      background: url(./assets/image/car2.png) no-repeat center / cover ;
      width: 636px;
      height: 550px;
      margin-top: 100px;
      margin-right: 20px;
    }

    /* media */

    @media screen and (max-width: 1281px){
      .header {
        max-width: 1281px;
        height: 1100px;
      }
    };

    @media screen and (max-width: 1167px){
      .banner{
        max-width: 1166px;
        width: 100%;
      }
      
      .banner .right{
        max-width: 550px;
      }

    };

    @media screen and (max-width: 1100px){
      .banner{
        max-width: 1100px;
        width: 100%;
      }
      
      .banner .right{
        max-width: 500px;
        margin-left: 20px;
      }

      .banner .left{
        margin-left: 20px;
      }

    };

    @media screen and (max-width: 1000px){
      .banner {
        max-width: 1000px;
        width: 100%;
      }

      .banner .right{
        max-width: 600px;
        width: 100%;
      }

      .banner .left .container .wrapper .title{
        font-size: 15px;
        max-width: 400px;
        width: 100%;
        margin-left: 10px;
      }

      .left .container .wrapper .image_text{
        max-width: 400px;
        width: 100%;
        gap: 20px;
        
      }
    };

    @media screen and (max-width: 967px){

      .header{
        max-width: 967px;
        height: 1600px;
      }

      .header .navbar .links{
        display: none;
      }

      .header .navbar .action_btn{
        display: none;
      }

      .header .dropdown_menu{
        display: block;
      }

      .header .navbar .toggle_btn{
        display: block;
      }
    };

    @media screen and (max-width: 821px){
      .header{
        max-width: 821px;
        height: 1500px;
      }
    };

    @media screen and (max-width: 801px){
      .header {
        max-width: 800px;
      }

      .header .container{
        max-width: 800px;

      }

      .header .container .left .box{
        max-width: 200px;
      }

      .header .container .left .box .layout{
        max-width: 200px;
      }
    };

    @media screen and (max-width: 769px) {
      .header{
        max-width: 769px;
        height: 1300px;
      }

      .header .navbar .links{
        display: none;
      }

      .header .navbar .toggle_btn{
        display: block;
      }

      .dropdown_menu{
        display: block;
      }
      .header .navbar .action_btn{
        display: none;
      }

      .banner{
        max-width: 769px;
        width: 100%;
        display: flex;
        flex-direction: column;
        height: 100%;
      }

      .banner .left{
        max-width: 700px;
        width: 100%;
        margin: 0 auto;
      }

      .banner .left .container{
        max-width: 700px;
        width: 100%;
      }

      .banner .left .container .wrapper{
        max-width: 700px;
        width: 100%;
      }

      .banner .left .container .wrapper .image_text{
        max-width: 700px;
        width: 100%;
        gap: 6px;
      }

      
        .banner .left .container .wrapper .title{
        font-size: 20px;
        max-width: 700px;
        width: 100%;
        margin-left: 10px;
        text-align: center;
      }

      .banner .right{
        max-width: 700px;
        width: 100%;
        margin: 80px auto;
      }

      
      
    };

    @media screen and (max-width: 726px){
      .header {
        max-width: 725px;
      }

      .header .container{
        max-width: 725px;

      }

      .header .container .left .box{
        max-width: 200px;
      }

      .header .container .left .box .layout{
        max-width: 200px;
      }

      
     
    };  
    
    @media screen and (max-width: 731px){
      .banner {
        max-width: 730px;
        width: 100%;
      }

      .banner .left{
       margin-left: -6px;
       
      }

      .banner .left .container .wrapper .title{
        max-width: 500px;
        width: 100%;
        margin-left: 80px;
      }

      .banner .left .container .wrapper .image_text{
        max-width: 500px;
        margin-left: 100px;
        
      }
      
      .banner .left .container .wrapper{
        display: flex;
        gap: 20px;
        flex-direction: column;
      }

      .banner .right{
        margin-top: 120px;
      }
    };

    @media screen and (max-width: 701px){
      .header {
        max-width: 700px;
        height: 1200px;
      }

      .header .container{
        display: flex;
        flex-wrap: wrap;
        max-width: 669px
        
      }

      .header .container .left{
        max-width: 250px;
        margin-left: 30px;
      }

      .header .container .center{
        max-width: 250px;
        margin-left: 30px;
      }

      .header .container .right{
        max-width: 250px;
        margin-left: 180px;
      }
        
    };

    @media screen and (max-width: 644px){
      .header {
        max-width: 644px;
        height: 1200px;
      }

      .header .container{
        max-width: 644px;
        display: flex;
        flex-wrap: wrap;
      }

      .header .container .left {
        max-width: 220px;
      }

      .header .container .center{
        max-width: 220px;
      }

      .header .container .right{
        max-width: 220px;
        margin-left: 165px;
      }
      
    };

    @media screen and (max-width: 595px){
      .banner{
        max-width: 594px;
        width: 100%;
      }

      .banner .left{
        margin-left: -40px;
      }

      
    };

    @media screen and (max-width: 584px){
      .header {
        max-width: 584px;
      }

      .header .container{
        max-width: 584px;
        display: flex;
        flex-wrap: wrap;
      }

      .header .container .left{
        max-width: 210px;
      }

      .header .container .center{
        max-width: 210px;
      }

      .header .container .right{
        max-width: 210px;
      }
    };

    @media screen and (max-width: 565px){
      .header{
        max-width: 564px;
      }

      .header .container{
        max-width: 564px;
      }

      .header .container .left{
        max-width: 220px;
        margin-left: 5px;
      }

      .header .container .center{
        max-width: 200px;
      }

      .header .container .right{
        max-width: 200px;
        margin-left: 130px;
      }

      .banner{
        max-width: 564px;
        width: 100%;
      }

      .banner .left .container .wrapper .image_text{
        display: flex;
        flex-direction: column;
        margin: 50px 0 0 40px;
        width: 500px;
        text-align: center;
      }

      .banner .left .container .wrapper .title{
        margin-left: 50px;
      }

      .banner .right{
        margin-top: 300px;
      }
 
      
    };

    @media screen and (max-width: 541px){

      .header{
        max-width: 541px;
      }

      .header .text_logo{
        max-width: 540px;
      }

      .header .text_logo .text{
        margin-left: 5px;
      }

      .header .container{
        max-width: 541px;
      }

      .header .container .left{
        margin-left: -8px;
      }

      .header .container .right{
        margin-left: 120px;
      }

    };

    @media screen and (max-width: 531px){
      .header{
        max-width: 531px;
      
      }

      .header .container{
        max-width: 500px;
        margin-left: -8px;
      }
      
      .banner{
        max-width: 531px;
        width: 100%;
      }

      .banner .left .container .wrapper .title{
        max-width: 350px;
        width: 100%;
        font-size: 15px;
        margin-left: 90px;
      }

      .banner .left .container .wrapper .image_text{
        margin-left: 40px;
      }

      
    };
    
    @media screen and (max-width: 527px){
      .header {
       max-width: 527px;
       height: 1400px;
      }

      .header .container {
        max-width: 500px;
        margin-left: 6px;
      }

      .header .container .left{
        margin: 0 auto;
        max-width: 500px;
        width: 100%;  
      }

      .header .container .center{
        margin: 0 auto;
        max-width: 500px;
        width: 100%;  
      }

      .header .container .right{
        margin: 0 auto;
        max-width: 500px;
        width: 100%;  
      }
      
    };

    @media screen and (max-width: 521px){
      .header{
        max-width: 521px;
      }

      .header .text_logo{
        max-width: 520px;
        margin-left: -20px;
      }
    };

    @media screen and (max-width: 511px){
      .header{
        max-width: 510px;
        height: 1500px;
      }

      .header .text_logo{
        max-width: 510px;
        margin-left: -30px;
      }

      .header .container{
        max-width: 510px;
      }

      .header .container .left{
        margin: 0 auto;
        max-width: 500px;
        width: 100%;
      }

      .header .container .center{
        margin: 0 auto;
        max-width: 500px;
        width: 100%;
      }

      .header .container .right{
        margin: 0 auto;
        max-width: 500px;
        width: 100%;
      }

    };

    @media screen and (max-width: 506px){
      .header {
        max-width: 506px;
        height: 1400px;
      }

      .header .container{
        max-width: 506px;
      }

      .header .container .left{
        margin: 0 auto;
        max-width: 500px;
        width: 100%;
      }

      .header .container .center{
        margin: 0 auto;
        max-width: 500px;
        width: 100%;
      }

      .header .container .right{
        margin: 0 auto;
        max-width: 500px;
        width: 100%;
      }


      
    };

    @media screen and (max-width: 500px){
      .header{
        max-width: 500px;
      }

      .header .text_logo{
        max-width: 400px;
        margin-left: -40px;
      }

      .header .text_logo .text{
        font-size: 40px;
        margin-left: 110px;
      }

      .header .navbar .toggle_btn{
        margin-right: 30px;
      }

      .header .navbar .toggle_btn{
        margin-top: -20px;
      }

      .header .container {
        max-width: 400px;
        width: 100%;
        margin: 30px 20px 0 0;
      }

      .header .container .left .box .layout{
        font-size: 18px
      }

      .header .container .right .box .job1{
        font-size: 18px;
        text-align: center;
      }

      .header .container .right .box .job2{
        font-size: 18px;
        text-align: center;
      }

      .banner {
        max-width: 500px;
        width: 100%;
      }

      .banner .left .container .wrapper .image_text{
        max-width: 300px;
        width: 100%;
        margin-left: 120px;
      }

      .banner .left .container .wrapper .title{
        max-width: 300px;
        width: 100%;
        margin-left: 120px;
      }

      .banner .left .container .wrapper .image_text .text{
        font-size: 23px;
      }
    };

    @media screen and (max-width: 444px){
      .banner {
        max-width: 444px;
        width: 100%;
      }

      .banner .left .container .wrapper{
        max-width: 500px;
        width: 100%;
        margin-right: 60px;
      }
    };

    @media screen and (max-width: 431px) {
      .header{
        max-width: 431px;
      }

      .header .container {
        max-width: 431px
      } 

      .header .container .left{
        max-width: 400px;
      }

      .header .container .left .box{
        max-width: 200px;
      }

      .header .container .center .box{
        max-width: 431px;
      }

      .header .container .right .box{
        max-width: 431px;
      }

      .header .container .left .box .layout{
        font-size: 20px;
        font-weight: 400
      }
    };
   
    @media screen and (max-width: 425px){
      .header{
        display: block;
        max-width: 425px;
      }

      .header .text_logo{
        max-width: 400px;
      }
      
      .header .text_logo .text{
        max-width: 400x;
        font-size: 50px;
        margin-left: 80px;
      }

      .header .text_logo .layout{
        max-width: 400px;
        font-size: 20px;
        margin-left: 20px;
      }

      .header .text_logo .btn{
        margin-left: 170px;
      }

      .header .container{
        max-width: 420px;
        margin-left: 3px;
      }

      

      .header .container .left{
        max-width: 300px;
        width: 100%;
      }

      .header .container .center{
        max-width: 300px;
        width: 100%;
      }

      .header .container .right{
        max-width: 300px;
        width: 100%;
        margin: 0 auto;
      }
    };

    @media screen and (max-width: 415px){
      .header .navbar .logo{
        display: none;
      }

      .header .text_logo{
        max-width: 410px;
        margin-right: 20px;
      }

      .header .text_logo .layout{
        max-width: 400px;
        margin-left: 10px;
      }

      .header .container{
        max-width: 410px;
        margin-left: 3px;
      }

      .header .container .left .box .layout{
        font-size: 20px;
        font-weight: 500;
      }

      .header .container .left{
        max-width: 300px;
        width: 100%;
        margin: 0 auto;
      }

      .header .container .center{
        max-width: 300px;
        width: 100%;
        margin: 0 auto;
      }

      .header .container .right{
        max-width: 300px;
        width: 100%;
        margin: 0 auto;
      }

      .header{
        max-width: 413px;
        height: 1600px;
      }

    };

    @media screen and (max-width: 400px){
      .header{
        max-width: 400px;
      }

      .header .text_logo{
        max-width: 300px;
        margin-top: -70px;
      }

      .header .text_logo .text{
        width: 300px;
        font-size: 40px;
      }

      .header .text_logo .layout{
        width: 300px;
        font-size: 24px;
        font-weight: 400;
        margin-left: 40px;
      }

      .header .text_logo .btn{
        margin-top: 100px;
        margin-left: 120px;
      }

      .banner {
        max-width: 400px;
        width: 100%;
      }

      .banner .left {
        max-width: 300px;
        width: 100%;
      }

      .banner .left .container .wrapper .image_text .text{
        width: 200px;
       margin-bottom: 30px;
       color: red
      }
    };

    @media screen and (max-width: 394px){
      .header {
        max-width: 393px;
      }

      .header .container{
        max-width: 390px;
         margin-left: 2px;
      }

      .header .container .left .box .layout{
        font-size: 20px;
      }

      .header .container .left{
        max-width: 360px;
        width: 100%
      }

      .header .container .center{
        max-width: 360px;
        width: 100%;
        margin: 0 0 0 0px ;
      }

      .header .container .right{
        max-width: 360px;
        width: 100%;
        margin: 0 auto;
      }

    };

    @media screen and (max-width: 376px){
      .header{
        max-width: 376px;
        width: 100%;
      }

      .header .text_logo{
        max-width: 250px;
      }

      .header .text_logo .text{
        max-width: 250px;
      }

      .header .container {
        max-width: 250px;
        margin: 30px auto;
      }

      
    };

    @media screen and (max-width: 364px){
      .banner{
        max-width: 364px;
        width: 100%;
      }

      .banner .left .container .wrapper .title{
        margin-left: 90px;
        max-width: 350px;
        width: 100%;
      }

      .banner .left .container .wrapper .image_text{
        margin-left: 80px;
      }
    };

    @media screen and (max-width: 340px){
      .header{
        max-width: 340px;
      } 

      .header .text_logo{
        max-width: 340px;
      }

      .header .text_logo .text{
        margin-left: 50px;
      }

      .header .text_logo .layout{
        margin-left: 20px;
      }

      .header .text_logo .btn{
        margin-right: 20px;
      }

      .header .container{
        margin-left: 3px;
      }
    };

    @media screen and (max-width: 331px){
      .header{
        max-width: 330px;
      }

      .header .text_logo{
        max-width: 250px;
      }

      .header .text_logo .text{
        max-width: 250px;
      }

      .header .text_logo .btn{
        margin-left: 120px;
      }

      .header .container{
        max-width: 300px;
        margin-left: 3px;
      }

      .header .container .left{
        
        max-width: 300px;
        width: 100%;
      }

    };

    @media screen and (max-width: 321px){
      .header {
        max-width: 321px;
        width: 100%;
        height: 1300px;
      }

      .header .container{
        max-width: 300px;
        width: 100%;
        margin-left: 0;
      }


      .banner {
        max-width: 320px;
        width: 100%;
      }

      .banner .left .container .wrapper .title{
        margin-left: 90px;
        max-width: 250px;
        width: 100%;
        margin-bottom: 20px;
      }
      
    };

    @media screen and (max-width: 310px){
      .header{
        max-width: 310px;
      }

      .header .text_logo{
        max-width: 200px;
        margin-left: -50px;
      }

      .header .text_logo .text{
        max-width: 200px;
        font-size:35px
      }

      .header .text_logo .btn{
        margin-left: 100px;
      }


    };
    
    @media screen and (max-width: 301px){
      .header {
        max-width: 300px;
      }

      .header .text_logo{
        margin-top: -100px;
        margin-left: -30px;
      }

      .header .text_logo .layout{
        width: 250px;
        font-size: 24px;
      }

      .banner {
        max-width: 300px;
        width: 100%;
      }

      .banner .left .container .wrapper .title{
        margin-left: 80px;
      }

      .banner .left .container .wrapper .image_text{
        margin-left: 70px;
      }
      
    };

    @media screen and (max-width: 281px){
      .header{
        max-width: 280px;
      }

      .header .text_logo{
        max-width: 280px;
        margin-left: -40px;
      }
    };
  


</style>