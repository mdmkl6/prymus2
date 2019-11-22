<template>
  <div>  
    Firstname:<input type="text" v-model="Firstname"></br>
    Lastname:<input type="text" v-model="Lastname"></br>
    <button @click="addNew()">Add new</button>
    <ul v-if="list.length>0">
      <li v-for="el in list">{{el}}</li>
    </ul>
  </div>
</template>
 
<script>
    export default {
        data() {
            return {list: []}
        },
        methods: {
            addNew(){
              this.list.push(this.Firstname+" "+this.Lastname);
            }
        }
    };
</script>