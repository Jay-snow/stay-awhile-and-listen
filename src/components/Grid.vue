<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
      <div id="board">
        <table>
          <tr v-for="block in grid">
              <td> {{ grid }} </td>
          </tr>
      
    </table>
    </div>

  </div>
</template>

<script>



export default {
  name: 'Grid',
  props: {
    msg: String,
    

  },
  data: function() { 
      return {
    grid: [ [0,0,0,0],[0,0,0,0],[0,0,0,0],[0,0,0,0] ],
    }
  },
  methods:{
        log: function() {
      console.log(this.grid);
      } 
  },

  created: function(){
    this.log();
 
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

#board {
  display:flex;
  justify-content: center;
}

#board table {
  font-size:30px;
}

h3 {
  margin: 40px 0 0;
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
</style>
