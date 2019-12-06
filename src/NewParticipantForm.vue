<template>
  <div>
    <form @submit.prevent="">
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
        this.newParticipant = this.Firstname +' '+this.Lastname;
        this.$emit('added', this.newParticipant);
      }
    }
  };
</script>