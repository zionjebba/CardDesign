<template>
  <div class="container">
    <div class="main">

      <div class="box">

        <div class="card1">
          <img src="../src/assets/perfume.jpg"  alt="">
        </div>
        <div class="card2">
          <h1 class="header">PERFUME</h1>

        <h2 class="sub-header"> Gabrielle <br> Essence Eau <br> De Parfum</h2>

        <p class="description"> Lorem ipsum dolor sit amet consectetur adipisicing elit. 
          Natus libero fugiat dolore inventore eligendi eaque.Lorem ipsum dolor, sit amet 
          consectetur adipisicing elit. Ex architecto consectetur, tempore nihil reprehenderit
           eveniet?</p>

        

        <p class="currency1"> $169.99</p>
        <p class="currency2"> $149.99</p>

        <button class="btn" @click="toggleButtonState">
            <span v-if="isButtonClicked">Remove</span>
            <span v-else>Add to Cart</span>
   
    
  </button> 
        </div>
        
      </div>
    </div>
    </div>

</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      isButtonClicked: false,
    };
  },
  methods: {
    toggleButtonState() {
      this.isButtonClicked = !this.isButtonClicked;
    },
  },
  components: {},
};
</script>

<style scoped>
*{
  margin: 0;
  padding: 0;
}

@import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,700&family=Montserrat:wght@200;300&display=swap');  
  @import url('https://fonts.googleapis.com/css2?family=Fraunces:opsz,wght@9..144,400;9..144,700&family=Montserrat:wght@200;300&display=swap');


.container {
  height: 100vh;
  width: 100%;
  background-color: hsl(30, 38%, 92%);
  display: flex;
  justify-content: center;
  align-items: center;
}

.main{
  width: 800px;
  height: 600px;
  background: white;
  border-radius: 16px;
}
.box{
  width: 100%;
  height: 100%;
  display: flex;
}

.card1{
width: 50%;
height: 100%;

}


.card1 img{
  width:100%;
  height: 100%;
  background: pink;
  border-top-left-radius: 16px;
  border-bottom-left-radius: 16px;  
}

.card2{
width:50%;
/* height: 100%; */
background: white;
border-top-right-radius: 16px;
border-bottom-right-radius: 16px;
padding: 20px;
display: flex;
flex-direction: column;
justify-content: gap;
}

h1{
  font-family: 'Monteserrat', sans-serif;
  letter-spacing: 3px;
  font-size: 1rem;
  margin-top: 20px;
}

h2{
  font-size: 2.2em;
  font-family: 'Fraunces', serif;
  font-weight: bolder;
  margin-top: 20px;
}

p{
  font-family: 'Fraunces', serif;
  width:90%;
flex-wrap: wrap;
font-size: 16px;
line-height: 1.5em;
margin-top: 25px;}



.currency1{
  margin-left: 32%; 
  font-size: smaller;
  text-decoration: line-through;
  
}

.currency2{
  font-size: 2em;
  color: hsl(158, 36%, 37%);
  margin-top: -20px;;
}


.btn{
margin-top: 30px ;
width: 300px;
height: 40px;
background: hsl(158, 36%, 37%);
border-radius: 6px;
cursor: pointer;
color: white;
font-family: sans-serif;
font-weight: bolder;
}

@media screen and (max-width: 600px) {
    .btn{
      color:red;
    }
    
  }

</style>

