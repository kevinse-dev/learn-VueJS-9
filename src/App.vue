<template>
  <!-- <div id="app">
    <button @click="showPopup = true" >Open to Popup</button>
    <popup-comp @close="closePopup" v-show="showPopup" />
  </div> -->
  <div id="app">

    <InputComp @modelValue="name"/>
    <input type="text" v-model="text">
  </div>
</template>

<script>

// import PopupComp from './Components/PopupComp.vue'
import InputComp from './Components/InputComp.vue'
export default {
  name: 'App',
  components: {
    // PopupComp
    InputComp

  },
  // data(){
  //   return{
  //     showPopup: false
  //   }
  // },
  // methods:{
  //   closePopup(name){
  //     this.showPopup = false
  //     console.log('name', name)
  //   }
  // }
  data(){
    return{
      name:'',
      text:''
    }
  },
  methods:{
    input(name){
      this.name = name
    }
  }


}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
