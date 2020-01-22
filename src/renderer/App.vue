<template>
  <div id="app">
   <h1>{{title}}</h1>
      
   <div id="photos">
   <img v-bind:src="cubes[number-1].url">    
      
    <p>Dobili ste broj {{cubes[number-1].name}}</p>

   </div>
    <button @click="cheking()"> Role </button>

  
  </div>
</template>

<script>

export default {
  name: 'app',
  data: function() {
    return{
      title:"Play cube",
      cubes:[
        { 
          value:1,
          name:'jedan',
          url:require('../assets/one.png'),
        },
        { 
          value:2,
          name:'dva',
          url:require('../assets/two.png'),
          
                 },
         { 
          value:3,
          name:'tri',
          url:require('../assets/three.png'),
                 }, 
        { 
          value:4,
          name:'cetri',
          url:require('../assets/four.png'),
        },
        { 
          value:5,
          name:'pet',
          url:require('../assets/five.png'),
                 },
        { 
          value:6,
          name:'sest',
          url:require('../assets/six.png'),
                  }
      ],
     number:1,
                
    }
    
  },
         methods:{
    cheking:function(){    
      this.number=Math.floor(Math.random()*6)+1;
      
}
}}
</script>

<style>
#app{ 
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  width: 500px;
  height: 500px;
  margin-left: 100px;
  padding: 50px;
 
  text-align: center;

}
p{
  font-size: 30px;
}
button{
  width: 150px;
  height: 50px;
  background-color: lightseagreen;
  margin:30px;
}
body{
    background-color: yellowgreen;
   
}
img{
  width: 150px;
}
</style>