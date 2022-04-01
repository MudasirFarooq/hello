<script>
export default {
  name : 'HelloWorld',
  data() {
    return {
      skills: [],
    };
  },
};
</script>

<template>
  <h1>Chaild Component 1</h1>
  <h2>Check / uncheck individual</h2>
  <div>
    <input
      type="checkbox"
      id="html"
      value="Html"
      v-model="skills"
    />
    <label for="html">Html</label><br>
    <input type="checkbox" id="css" value="CSS" v-model="skills" />
    <label for="css">CSS</label><br>
    <input type="checkbox" id="java" value="JAVA" v-model="skills" />
    <label for="java">JAVA</label><br>
  </div>
  <h4>{{skills}}</h4>
</template>

<style>
</style>
