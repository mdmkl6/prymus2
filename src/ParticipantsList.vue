<template>
  <div>
    <ol>
        <h1>Participants list</h1>
      <ul v-if="list.length>0">
        <li v-for="el in list">{{el}}</li>
      </ul>
    </ol>
  </div>
</template>

<script>
  export default {
    props: ['list']
  };
</script>