<template>
  <div>
    <form @submit.prevent="add()">
        Firstname:<input type="text" v-model="Firstname"></br>
        Lastname:<input type="text" v-model="Lastname"></br>
        <button @click="add()">Add new participant</button>
    </form>
  </div>
</template>

<script>
  export default {
    data() {
      return {newParticipant: {},
      Firstname: "",
      Lastname: ""
      };
    },
    methods: {
      add() {
        this.$emit('added', this.newParticipant);
        this.newParticipant.Firstname;
        this.newParticipant.Lastname;
      }
    }
  };
</script>