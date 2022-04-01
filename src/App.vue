<script>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
export default{
  name: 'App',
  data(){
    return{
      items : ['one','two','three','four'],
      selected:[],
      checked: false
    }
  },
  methods:{
    ischeck(){
      this.selected= []
      if(!this.checked){
        for(let i=0;i<this.items.length;i++){
          this.selected.push(this.items[i])
        }
      }
    },
    stat(){
      if(this.selected.length == this.items.length){
        this.checked = true
      }else{
        this.checked = false
      }
    }
  },
  components:{
    HelloWorld,
    TheWelcome,
    
  }
}
</script>

<template>
  <HelloWorld/>
  <TheWelcome/>
  <h3>On all Check / unchecked, "Check all" should be checked and unchecked accordingly.</h3>
  <input type="checkbox" id="checkall" @click="ischeck" v-model="checked">
  <label for="checkall">Checkall</label><br>
  <div v-for="item in items" :key="item">
    <input type="checkbox" :value="item" v-model="selected"  @change="stat">
    <label for="">{{item}}</label><br>
  </div>
  <h4>{{selected}}</h4>
</template>

<style>



</style>
