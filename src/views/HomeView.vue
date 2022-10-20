<template>
 
  
  <div>

    <div class="header1">
        <v-layout align-center>
          <a href="#top" class="logo" v-scroll-to="'#top'">     
            <div  >임채연의 포트폴리오</div>
            </a>
            <v-spacer></v-spacer>     
            <div >
              <a href="#about" class="text1" v-scroll-to="'#about'">     
              <v-btn class="text2" x-large text>About me                
              </v-btn></a> 
              <a href="#certificatePrize" class="text1" v-scroll-to="'#certificatePrize'">   
              <v-btn class="text2" x-large text>certificate</v-btn></a>
              <a href="#certificatePrize" class="text1" v-scroll-to="'#certificatePrize'">   
              <v-btn class="text2" x-large text>prize</v-btn></a>
              <a href="#project" class="text1" v-scroll-to="'#project'"> 
              <v-btn class="text2" x-large text>project</v-btn></a>
            </div>
        </v-layout>
    </div>




    <div  id="top" class="welcome">
    <div class="developer">
    <img src="image/developer.png" alt="개발자" height="150px">
   </div>
     <vue-typer class="welcomeText"
     :text='["Welcome! \nThis is Lim Chaeyeon`s portfolio"]'
     :repeat='0'
     initial-action='typing'
      :pre-type-delay='50'
      :type-delay='50'>
      
     </vue-typer>
    
    </div>

    <div id="about" class="top" style="background-image: url(image/chaeyeon.jpg);">
      <v-layout class="log" data-aos="fade-right" data-aos-delay="100" fill-height align-center justify-end >
        <v-text>
          About me!
          <p class="about">
            <img src="image/person.png" height="30px" width="33px" color="white"> name: 임채연<br>
            <img src="image/birth.png" height="35px" width="33px" color="white"> birth: 2001.01.15<br>
            <img src="image/email.png" height="25px" width="35px" color="white"> email: dlacodus0115@naver.com<br>
            <img src="image/education.png" height="25px" width="35px" color="white"> education: 명지전문대학교 정보통신공학과 졸업<br>
          </p>
          
        </v-text>
        
      </v-layout>
    </div>
   

   <div id="certificatePrize" class="component"  data-aos="fade-up" data-aos-delay="250">
    <div  class="certificate" >
      <div class="header">─certificate─</div>
        <div class="back">
          
           <v-flex >
            <div class="image" style="background-image: url(image/certificate.jpg);">
              <v-layout  class="text"  >
                <br>
                 ▫ 정보처리기사 <br>
                 ▫ SQLD <br>
                 ▫ Adobe Certified Professional (ACP) <br>  &nbsp;&nbsp;&nbsp; Illustrator CC & InDesign CC<br>
                 ▫ 파이썬프로그래밍활용능력2급<br>
                 ▫ 빅데이터분석실무2급<br>
              </v-layout>
            </div>            
           </v-flex>          
       </div>
      </div>
       <div  class="prize">
        <div class="header">─prize─</div>
         <div class="back">          
           <v-flex  >
            <div class="image" style="background-image: url(image/prize2.png);">
              <v-layout class="text" >
                <br>
                 ▫ 2020 경진대회 대상 <br>
                 ▫ 제13회 대한민국 세계<br>  &nbsp;&nbsp;&nbsp; 여성발명대회 은상 <br>
              </v-layout>
            </div>            
           </v-flex>          
       </div>
      </div>
     
    </div>

    <div id="project" class="project" >
      <div class="header">─project─</div>
        <v-layout  align-center class="pj1"  data-aos="fade-left" data-aos-delay="250"> 
          <a  style="text-decoration: none; color: white;"  href="https://play.google.com/store/apps/details?id=com.ejbt.smartdriving" >   
          <!-- <img src="image/smartDrive.jpg" class="image">      -->
          <div style="background-image: url(image/smartDrive.jpg);" class="image">
            <v-layout text class="link"  fill-height align-center justify-center>바로가기></v-layout>
          </div>
        </a>        
              <div class="text" >
                <br><h1>스마트 드라이브</h1> 
                
                운전자 모바일 GPS를 연계하여 스마트운전의 사회적 환경 비용을 실시간으로 모니터링하며
                자동차 운전 행태에 따른 임계치 초과에 따른 표준안전운전지수 등을 나타내 
                실시간 대기환경정보를 제공함으로써 운행 차량 배출 감소
              
                 
              </div>
             
        </v-layout>    
        <v-layout align-center class="pj2" data-aos="fade-right" data-aos-delay="250">               
        <a  style="text-decoration: none; color: white;"  href="https://play.google.com/store/apps/details?id=seoul.gangseo.gsnavi" >   
          <!-- <img src="image/smartDrive.jpg" class="image">      -->
          <div style="background-image: url(image/nav.jpg);" class="image">
            <v-layout text class="link"  fill-height align-center justify-center>바로가기></v-layout>
          </div>
        </a>        
          <div class="text" >
                <br><h1>강서마곡 보행자내비</h1>                 
                강서구 마곡지구 내에서 도보로 이동하는 보행자를 위한 길안내 어플리케이션으로
                목적지를 검색하고 내비게이션의 안내에 따라 최적의 경로로 이동
              
                 
            
                
              </div>
        </v-layout>     
      
    </div>



</div>

</template>

<script>
import { Swiper, SwiperSlide } from 'vue-awesome-swiper'  
import 'swiper/swiper-bundle.css'
import AOS from "aos"
import "aos/dist/aos.css"

  export default {
    name: 'Home',
    data(){
      return{
        swiperOption:{
          loop:true,
          autoplay:{
            delay:3000
          }
        }
      }
    },
    mounted(){
      AOS.init()
    },
    components:{
      Swiper,
      SwiperSlide
    }
  }
</script>
<style scoped lang="less">
@import url("C:\Users\smile\Downloads\portpolio\portpolio\src\font\font.css");
*{font-family: 'GangwonEdu_OTFBoldA';}
.welcome{
  height: 90vh;
  padding: 15% 0% 0% 10%;
  .developer{
    padding-block-end: 30px;
    
  }
  .welcomeText{
    
      font-size:90px;
    }
}

.component{
  padding-top:80px ;
  display: flex;
  flex-direction: row;
  height: fit-content;
  
.certificate{
  width: 50%; 
  padding-left: 15%;
  padding-right: 1.5%;
  float: right;
  
  .header{    
    text-align: center;
    font-size:  70px;
    font-weight: bold;    
  }
  .back{     
    
      .image{            
         background-size: 250px 250px;
         background-position: right;
         .text{
           font-size: 30px;             
           color: black;  
          }            
       }
    }
  }

  
.prize{
  width: 50%;
  padding-right: 15%;
  padding-left: 1.5%;
  float: left;
  .header{    
    text-align: center;
      font-size: 70px;
      font-weight: bold;   
     }
  .back{     
      .image{   
        padding: 50px;
        background-size: 250px 250px;           
        background-position: right;        
       .text{
          font-size: 30px;          
          color: black;}            
      }
    }
  }
}



.project{
  padding-bottom: 100px;
  padding-top: 100px;
  .header{    
    text-align: center;
    font-size:  70px;
    font-weight: bold;
  }
  .pj1{
    display: flex;
    margin-right: 20%;
    flex-direction: row;
    margin-left: 20%;
    padding-bottom: 50px;
    


    .image{
      background-size: cover;
      height: 300px;
      width: 300px;
      // object-fit: cover;


      .link{
       visibility: hidden;
       text-decoration: none;
      }
    }

    .image:hover{
      box-shadow: inset 0 0 0 2000px rgba(0, 0, 0, 0.5);

      .link{
        visibility: visible;
        text-align: center;
        font-size: 40px;
        font-weight: bold;
        text-decoration: none;

      }

    }
    .text{
      padding-left: 30px;
      font-size: 25px;
    }
  }
  .pj2{ 
    display: flex;
    margin-right: 20%;
    flex-direction: row;
    margin-left: 20%;
    padding-bottom: 50px;
    .image{
      background-size: cover;
      height: 300px;
      width: 300px;
      // object-fit: cover;


      .link{
       visibility: hidden;
       text-decoration: none;
      }
    }

    .image:hover{
      box-shadow: inset 0 0 0 2000px rgba(0, 0, 0, 0.5);

      .link{
        visibility: visible;
        text-align: center;
        font-size: 40px;
        font-weight: bold;
        text-decoration: none;

      }

    }
    .text{
      font-size: 25px;
      padding-left: 30px;
    }
  }
}
  .top{
    
    height: 800px;
    background-size: cover;
    background-position: center center;
    .log{
      font-size: 80px;
        font-weight: bold;
        color: white;
        padding-right: 100px;
        .about{
          font-size: 30px;
          font-weight: normal;
        }
    }
  }
  

  .header1{
    z-index: 1;
        padding: 20px;
        box-shadow: 0 6px 6px #eee;
        background-color: white;
        position: fixed;
        top: 0;
        width: 100%;
        
       
           
            .logo{
              text-decoration: none;
              color: black;
              font-size: 30px;
              font-weight: bold;
              
              
            }
            .text1{
              text-decoration: none;
              color: black;
              height: 100%;
              .text2{
                font-size: 25px;

              }
                

            }

            
            .text1:hover{
              .text2{
                color: #fff;
                background-color: skyblue;
                transition: all .6s;
              }
              
              
            }
            
   }


    

</style>