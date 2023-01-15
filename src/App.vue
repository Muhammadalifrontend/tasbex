<template>
  <div>
    <div class="container">
      <p class="first"> {{title}} </p>
      <p class="second">Total: {{count}}</p>
      <p class="third">{{num}}</p>
      <button @click="countInc"  class="btn1">Count</button> <br>
      <button @click="countRes" class="btn2">Reset</button>
    </div>
  </div>
</template>


<script>

export default {

  data(){
    return{
      count: 0,
      title: 'Subhanalloh',
      num:0,
    }
  },
  methods:{
    countInc(){
      this.num++
      if(this.num===34){
        this.num=0
      }


      this.count++
      if(this.count>0 && this.count<=33){
        this.title='Subhanalloh'
      }
      else if(this.count>33 && this.count<=67){
        this.title='Alhamdulillah'
      }
      else if(this.count>67 && this.count<=99){
        this.title='Allohu akbar'
      }
      else if(this.count===100){
        this.count=0
      }
    },
    countRes(){
      this.count=0
      this.num=0
    }
  }
  
};
</script>

















<style>
.container{
  text-align: center;
  padding: 10px;
  margin:  auto;
  margin-top: 100px;
  height: 400px;
  width: 220px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 2);
}
.first{
  color: red;
  font-size: 20px;
}
.second{
  font-size: 20px;
  color: blueviolet;
  margin-top: 10px;
}
.third{
  font-size: 42px;
  color: blue;
}
.btn1{
  outline: none;
  width: 80px;
  height: 60px;
  border-radius: 50%;
  box-shadow: 0 2px 4px gray;
  border: none;
  background: rgb(95, 185, 185);
  font-size: 20px;
  font-weight: bold;
  cursor: pointer;
}
.btn2{
  margin-top: 20px;
  border-radius: 10px;
  outline: none;
  box-shadow: 0 2px 4px gray;
  border: none;
  background: rgb(95, 185, 185);
  font-size: 20px;
  font-weight: bold;
  cursor: pointer;
}


</style>
