<template>
  <div>
    <ol>
        <h1>Participants list</h1>
      <ul v-if="list.length>0">
        <li v-for="(el,key) in list">{{el}}
        <button type="button" class="btn btn-danger" @click="remove(list,el,key)">remove</button>
        </li>
      </ul>
    </ol>
  </div>
</template>

<script>
  export default {
    props: ['list'],
    methods: {
      remove(list,el,key) {
        console.log(key);
        list.splice(key,1);
      }
    } 
  };   
</script>