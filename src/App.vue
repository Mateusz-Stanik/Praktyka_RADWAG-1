<template>
  <h1 v-pre class="Recent" id="title">Pomiary</h1>
  <div id="container">
    <div class="looks">
        <h1 class="Top">Waga 1</h1>
        <div class="Data">
          <div class="Recent">
            <p class="Top">
              Masa
            </p>
            <p class="Bottom homer" @click="more1()" @click.right="less1()" style="font-size: 1.75vw;" id="measurement1">
              {{ mass[0] }}kg
            </p>
            <div class="Top">
              <img :src="image1" :style="Images"/>
              <img :src="image3" :style="Images"/>
              <img :src="image2" :style="Images"/>
            </div>
            <div class="Bottom-Wyk">
              <p class="Bottom homer" style="border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949; border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949;">0</p>
            </div>
          </div>
          <h3>Poprzednie Miary</h3>
          <div class="Prev">
            <p class="Top" :style="ToPrev">Masa</p>
            <p class="Top" :style="ToPrev">Czas</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-1">{{ Prev1[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-1">{{ timestamp1[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-2">{{ Prev1[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-2">{{ timestamp1[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-3">{{ Prev1[2] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-3">{{ timestamp1[2] }}</p>
          </div>
          <form @submit="submitForm()">
        <button class="Recent" :style="Button"  @click="update1()">Zapisz Pomiar</button>
      </form>
        </div>
    </div>
    <div class="looks">
        <h1 class="Top">Waga 2</h1>
        <div class="Data">
          <div class="Recent">
            <p class="Top">
              Masa
            </p>
            <p class="Bottom homer" @click="more2()" @click.right="less2()" style="font-size: 1.75vw;" id="measurement1">
              {{ mass[1] }}kg
            </p>
            <div class="Top">
              <img :src="image1" :style="Images"/>
              <img :src="image3" :style="Images"/>
              <img :src="image2" :style="Images"/>
            </div>
            <div class="Bottom-Wyk">
              <p class="Bottom homer" style="border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949; border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949;">0</p>
            </div>
          </div>
          <h3>Poprzednie Miary</h3>
          <div class="Prev">
            <p class="Top" :style="ToPrev">Masa</p>
            <p class="Top" :style="ToPrev">Czas</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-1">{{ Prev2[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-1">{{ timestamp2[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-2">{{ Prev2[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-2">{{ timestamp2[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-3">{{ Prev2[2] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-3">{{ timestamp2[2] }}</p>
          </div>
          <form @submit="submitForm()">
        <button class="Recent" :style="Button"  @click="update2()">Zapisz Pomiar</button>
      </form>
        </div>
    </div>
    <div class="looks">
        <h1 class="Top">Waga 3</h1>
        <div class="Data">
          <div class="Recent">
            <p class="Top">
              Masa
            </p>
            <p class="Bottom homer" @click="more3()" @click.right="less3()" style="font-size: 1.75vw;" id="measurement1">
              {{ mass[2] }}kg
            </p>
            <div class="Top">
              <img :src="image1" :style="Images"/>
              <img :src="image3" :style="Images"/>
              <img :src="image2" :style="Images"/>
            </div>
            <div class="Bottom-Wyk">
              <p class="Bottom homer" style="border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949; border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949;">0</p>
            </div>
          </div>
          <h3>Poprzednie Miary</h3>
          <div class="Prev">
            <p class="Top" :style="ToPrev">Masa</p>
            <p class="Top" :style="ToPrev">Czas</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-1">{{ Prev3[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-1">{{ timestamp3[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-2">{{ Prev3[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-2">{{ timestamp3[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-3">{{ Prev3[2] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-3">{{ timestamp3[2] }}</p>
          </div>
          <form @submit="submitForm()">
        <button class="Recent" :style="Button"  @click="update3()">Zapisz Pomiar</button>
      </form>
        </div>
    </div>
    <div class="looks">
        <h1 class="Top">Waga 4</h1>
        <div class="Data">
          <div class="Recent">
            <p class="Top">
              Masa
            </p>
            <p class="Bottom homer" @click="more4()" @click.right="less4()" style="font-size: 1.75vw;" id="measurement1">
              {{ mass[3] }}kg
            </p>
            <div class="Top">
              <img :src="image1" :style="Images"/>
              <img :src="image3" :style="Images"/>
              <img :src="image2" :style="Images"/>
            </div>
            <div class="Bottom-Wyk">
              <p class="Bottom homer" style="border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949; border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949;">0</p>
            </div>
          </div>
          <h3>Poprzednie Miary</h3>
          <div class="Prev">
            <p class="Top" :style="ToPrev">Masa</p>
            <p class="Top" :style="ToPrev">Czas</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-1">{{ Prev4[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-1">{{ timestamp4[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-2">{{ Prev4[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-2">{{ timestamp4[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-3">{{ Prev4[2] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-3">{{ timestamp4[2] }}</p>
          </div>
          <form @submit="submitForm()">
        <button class="Recent" :style="Button"  @click="update4()">Zapisz Pomiar</button>
      </form>
        </div>
    </div>
    <div class="looks">
        <h1 class="Top">Waga 5</h1>
        <div class="Data">
          <div class="Recent">
            <p class="Top">
              Masa
            </p>
            <p class="Bottom homer" @click="more5()" @click.right="less5()" style="font-size: 1.75vw;" id="measurement1">
              {{ mass[4] }}kg
            </p>
            <div class="Top">
              <img :src="image1" :style="Images"/>
              <img :src="image3" :style="Images"/>
              <img :src="image2" :style="Images"/>
            </div>
            <div class="Bottom-Wyk">
              <p class="Bottom homer" style="border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949; border-right: 1px solid #0b4949;">0</p>
              <p class="Bottom homer" style="border-left: 1px solid #0b4949;">0</p>
            </div>
          </div>
          <h3>Poprzednie Miary</h3>
          <div class="Prev">
            <p class="Top" :style="ToPrev">Masa</p>
            <p class="Top" :style="ToPrev">Czas</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-1">{{ Prev5[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-1">{{ timestamp5[0] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-2">{{ Prev5[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-2">{{ timestamp5[1] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousMasa-1-3">{{ Prev5[2] }}</p>
              <p class="Bottom" :style="BotPrev" id="PreviousTime-1-3">{{ timestamp5[2] }}</p>
          </div>
          <form @submit="submitForm()">
                          <button class="Recent" :style="Button"  @click="update5()">Zapisz Pomiar</button>
          </form>
        </div>
    </div>
  </div>
  <div>
    <h3 id="Pomiar" class="Top">Średnia Wszystkich Pomiarów</h3>
    <p id="Pomiar" class="Bottom homer">0kg</p>
  </div>
</template>

<script>
import image1 from "./assets/stability.png";
import image2 from "./assets/weight.png";
import image3 from "./assets/zero.png";

  export default {
    data() {
      return {
        Prev1: ['', '', ''],
        Prev2: ['', '', ''],
        Prev3: ['', '', ''],
        Prev4: ['', '', ''],
        Prev5: ['', '', ''],
        
        timestamp1: ["","",""],
        timestamp2: ["","",""],
        timestamp3: ["","",""],
        timestamp4: ["","",""],
        timestamp5: ["","",""],

        mass: [0, 0, 0, 0, 0],
        temp: "",
        add: 0,
        pomiar: 0,

        image1: image1,
        image2: image2,
        image3: image3,

        ToPrev: 'width: 100%; border-bottom: 2px solid #0b4949;',
        BotPrev: 'border-top: 0',
        Images: 'width:1.4vw; height:auto; margin-left: auto; margin-right: auto;',
        Button: 'padding: 0.5vh 0.5vw; font-size: 1vw; font-weight: bold'
      }
    },
    created() {
      setInterval(this.getNow, 100);
    },
    methods: {
      submitForm() {
        event.preventDefault()
      },
      
      pomiarowo() {
        this.add+=this.masa[0]
        // this.add+=this.masa[1]
        // this.add+=this.masa[2]
        // this.add+=this.masa[3]
        // this.add+=this.masa[4]
        // this.pomiar=(this.temp/5)
      },
      
      update1() {
        this.Prev1[2]=this.Prev1[1];
        this.Prev1[1]=this.Prev1[0];
        this.Prev1[0]=this.mass[0]+"kg";
        
        this.timestamp1[2]=this.timestamp1[1];
        this.timestamp1[1]=this.timestamp1[0];
        this.timestamp1[0]=this.temp;
      },
      update2() {
        this.Prev2[2]=this.Prev2[1];
        this.Prev2[1]=this.Prev2[0];
        this.Prev2[0]=this.mass[1]+"kg";
        
        this.timestamp2[2]=this.timestamp2[1];
        this.timestamp2[1]=this.timestamp2[0];
        this.timestamp2[0]=this.temp;
      },
      update3() {
        this.Prev3[2]=this.Prev3[1];
        this.Prev3[1]=this.Prev3[0];
        this.Prev3[0]=this.mass[2]+"kg";
        
        this.timestamp3[2]=this.timestamp3[1];
        this.timestamp3[1]=this.timestamp3[0];
        this.timestamp3[0]=this.temp;
      },
      update4() {
        this.Prev4[2]=this.Prev4[1];
        this.Prev4[1]=this.Prev4[0];
        this.Prev4[0]=this.mass[3]+"kg";
        
        this.timestamp4[2]=this.timestamp4[1];
        this.timestamp4[1]=this.timestamp4[0];
        this.timestamp4[0]=this.temp;
      },
      update5() {
        this.Prev5[2]=this.Prev5[1];
        this.Prev5[1]=this.Prev5[0];
        this.Prev5[0]=this.mass[4]+"kg";
        
        this.timestamp5[2]=this.timestamp5[1];
        this.timestamp5[1]=this.timestamp5[0];
        this.timestamp5[0]=this.temp;
      },



      more1() {
        this.mass[0]++
      },
      more2() {
        this.mass[1]++
      },
      more3() {
        this.mass[2]++
      },
      more4() {
        this.mass[3]++
      },
      more5() {
        this.mass[4]++
      },


      
      less1() {
        this.mass[0]--
      },
      less2() {
        this.mass[1]--
      },
      less3() {
        this.mass[2]--
      },
      less4() {
        this.mass[3]--
      },
      less5() {
        this.mass[4]--
      },
      

      
      getNow() {
        const today = new Date();
        const time = today.getHours() + ":" + today.getMinutes();
        this.temp = time;
      }
    }
  }
</script>

<style>
  *{
    box-sizing: border-box;
}
html{
    height: 100%;
    width: 100%;
}
body{
    overflow-x: visible;
    background-color: #add8e6;
    font-family: sans-serif;
    font-weight: bold;
    font-size: 1.5vw;
}
#title{
    margin-left: auto;
    margin-right: auto;
    text-align: center;
    background-color: #0b494980;
    min-width: 99vw;
    height: auto;
    font-size: 3.5vw;
    padding: 1vh 0;
}
#container{
    overflow-x: visible;
    margin-left: auto;
    margin-right: auto;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    max-height: 80vh;
    min-width: 99vw !important;
    height: auto;
}
.looks{
    overflow-x: visible;
    border-radius: 15px;
    background: #add8e600;
    min-height:60vh !important;
    min-width: 20vw !important;
    display: inline-block;
    padding: 1.5vw;
    margin: 0 auto;
}
.looks:hover {
    animation-name: glowout;
    animation-duration: 1.5s;
    animation-iteration-count: infinite;
  }
.Data{
  overflow-x: visible;
    border-radius: 15px;
    background: #add8e6;
    min-height:60vh !important;
    min-width: 20vw !important;
    display: inline-block;
    padding: 1.5vw;
    margin: 0 auto;
    overflow-x: visible;
    min-height:66vh !important;
    min-width: 100% !important;
    display: inline-block;
    margin: 0 auto;
    background-color: #e0ffff;
    padding: 2vw 2vw;
}
.Recent{
    padding: 0.075vw;
    border: 2px solid #0b4949;
    border-radius: 5px;
    margin-top: 0;
    margin-bottom: 0;
    margin-left: auto;
    margin-right: auto;
}
.Prev{
    display: grid; 
    grid-auto-columns: 1fr; 
    grid-template-columns: 1fr 1fr; 
    grid-template-rows: 1fr 1fr 1fr 1fr; 
    gap: 0; 
    grid-template-areas: 
      "Top Top"
      "Bottom Bottom"
      "Bottom Bottom"
      "Bottom Bottom"; 
    justify-content: center;
    flex-direction: row;
    align-items: center;
    align-content: center;
    border: 2px solid #0b4949;
    border-collapse: collapse;
    border-radius: 5px;
    margin-left: auto;
    margin-right: auto;
    padding: 1px;
}
.Top{
    display: flex;
    justify-content: center;
    flex-direction: row;
    align-items: center;
    align-content: center;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    border: 2px solid #0b4949;
    border-bottom: 1px solid #0b4949;
    background-color: #0b494980;
    margin-left: auto;
    margin-right: auto;
    margin-top: 0;
    margin-bottom: 0;
    padding: 0;
}
.Bottom{
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
    border: 2px solid #0b4949;
    border-top: 1px solid #0b4949;
    margin-top: 0;
    margin-bottom: 0;
    padding: 0;
}
.Bottom-Wyk{
    display: flex;
    margin-top: 0;
    margin-bottom: 0;
    padding: 0;
    margin-left: auto;
    margin-right: auto;
}
.Bottom.homer{
    margin-top: 0;
    margin-bottom: 0;
    width: 100%;
    margin-left: auto;
    margin-right: auto;
    border-right: 2px solid #0b4949;
    border-left: 2px solid #0b4949;
}
.Srednia{
    border: 2px solid #0b4949;
    border-radius: 5px;
}
#Pomiar{
    margin-left: auto;
    margin-right: auto;
    justify-content: center;
    align-items: center;
    text-align: center;
    margin: 0 auto;
    background-color: #e0ffff;
    justify-content: center;
    align-items: center;
    text-align: center;
    width:50vw;
    height: auto;
    font-size: 1.35vw;
    padding: 1vh 0;
}
#Pomiar.Top{
    display: flex;
    justify-content: center;
    flex-direction: row;
    align-items: center;
    align-content: center;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    border: 2px solid #0b4949;
    border-bottom: 1px solid #0b4949;
    background-color: #0b494980;
    margin-left: auto;
    margin-right: auto;
    margin-top: 0;
    margin-bottom: 0;
    padding: 0;
}
.homer{
    background-color: #e0ffff;
}
.Bottom:hover{
    animation-name: sredni;
    animation-duration: 1s;
    animation-iteration-count: infinite;
}
.Bottom.homer:hover{
    transform: scale(1.3);
    transition: 0.3s ease-in;
}
#Pomiar.Bottom.homer:hover{
    transform: scale(1.1);
    transition: 0.3s ease-in;
    animation-name: sredni;
    animation-duration: 1s;
    animation-iteration-count: infinite;
}
@media screen and (max-width: 1308px){
    #container {
         width:50vw;
     }
     .looks{
         width: 100vw;
         margin:0 auto;
         height: auto;
     }
 }
@media screen and (max-width: 1024px){
    #title{
        width: 80vw;
        margin:0 auto;
        height: auto;
    }
   #container {
        overflow: visible;
        display: flex;
        flex-direction: column;
        margin:0 auto;
        width:auto;
        font-size: larger;
        min-height: 300vh;
    }
    .looks{
        width: 99vw;
        margin:0 auto;
        height: auto;
    }
    .Data{
        min-height:60vh !important;
        width: 90vw !important;
        margin: 0 auto;
    }
    img{
        width: 2vw;
    }
    #Pomiar{
        visibility: hidden;
    }
}
@keyframes glowit {
    0% {box-shadow: 0px 0px 5px 0px rgba(120,120,120,0.75);}
    50% {box-shadow: 0px 0px 5px 10px rgba(120,120,120,0.75);}
    100% {box-shadow: 0px 0px 5px 0px rgba(120,120,120,0.75);}
}
@keyframes glowout {
    0% {background-color: #add8e600;}
    50% {background-color: #e0ffff80;}
    100% {background-color: #add8e600;}
}
@keyframes sredni {
    0% {background-color: #e0ffff;}
    50% {background-color: #76a4a4;}
    100% {background-color: #e0ffff;}
}
</style>