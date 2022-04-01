<script>
export default {
  name: "TheWellcome",
  data() {
    return{
    options: ["html", "css", "javs", "php", "javascript"],
    selected: [],
    selectAll: false,
    }
  },
  methods: {
    select() {
      this.selected = [];
      if (!this.selectAll) {
        for (let i in this.options) {
          this.selected.push(this.options[i]);
        }
      }
    },
  }
};
</script>

<template>
  <h1>Chaild Component 2</h1>
  <h2>Check / uncheck all</h2>
    

  <input type="checkbox" v-model="selectAll" @click="select()" /> Select all
    <div v-for='option in options' :key="option">
      <label>  <input type="checkbox" :value="option" v-model="selected">{{ option }}</label>

    </div>
    <h4>{{selected}}</h4>
</template>
