<template>
  <div>

    <div class="row">
      <input v-model.number="num1" type="number"/>
      <span>+</span>
      <input v-model.number="num2" type="number"/>
      <span>=</span>
      <h3>{{ num1 + num2 }}</h3>
    </div>
    <hr />
    <div class="row">
      <select v-model="name">
        <option>React</option>
        <option>Vue</option>
        <option>Ember</option>
        <option>Angular</option>
      </select>
      
    </div>
    <h3 v-if="name"> My favorite framework is {{ name }}</h3>
</div>
</template>

<script>
export default {
  name: 'Calculator',
  data(){
    return {
      num1: 1, 
      num2: 2, 
      name: ""
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  font-size: 30px; 
  color: #41b883; 
  margin: 0 10px;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.row {
  margin: 40px 0; 
  display: flex; 
  align-items: center; 
  justify-content: center; 
  
}

input {
  width: 50px; 
  heigth: 5px; 
  margin: 0 10px; 
}

hr {
  width: 600px; 
  border: 1px solid #41b883; 
}
</style>
