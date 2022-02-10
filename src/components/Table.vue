<template>
  <div>
    <table>
      <tr>
        <th>created</th>
        <th>text</th>
        <th>type</th>
      </tr>
      <tr v-for="(animal, index) in animals" :key="index">
        <td>{{animal.createdAt}}</td>
        <td>{{animal.text}}</td>
        <td>{{animal.type}}</td>
      </tr>
    </table>

  </div>
</template>
<script>
export default {
  name:'Table',
  data(){
    return{
      animals:[]
    }
  },
  props:{
    type: String
  },
  created(){
    fetch(`https://cat-fact.herokuapp.com/facts/random?animal_type=${this.type}&amount=10`)
    .then(response => response.json())
    .then(data => {this.animals= data})

  }
}
</script>