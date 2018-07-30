<template>
  <div class="container">
    <div class="holder">
      <ul>
        <li v-for="(data,index) in skills" :key='index'>{{data.skill}}</li>
      </ul>

      <p v-if="skills.length >= 2"> You have more than 1 skill</p>
      <p v-else>Sucks to be you</p>
    </div>    
  <!-- <button v-on:click="changeName" v-bind:disabled=true> Cool disabled button</button> -->
  </div>
</template>

<script>
export default {
  name: 'Skills',
  data(){
    return{
      skills: [
        {'skill': 'Vue.js'},
        {'skill': 'Other'}
        ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

  .holder {
    background: #fff;
  }

  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
  }
  
  ul li {
    padding: 20px;
    font-size: 1.3em;
    background-color: #E0EDF4;
    border-left: 5px solid #3EB3F6;
    margin-bottom: 2px;
    color: #3E5252;
  }

  p {
    text-align:center;
    padding: 30px 0;
    color: gray;
  }

  .container {
    box-shadow: 0px 0px 40px lightgray;
  }

</style>