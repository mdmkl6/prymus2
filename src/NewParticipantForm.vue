<template>
  <div>
    <form @submit.prevent="">
      <div class="form-group">
        Firstname:<input class="form-control" type="text" v-model="Firstname"></br>
        Lastname:<input class="form-control" type="text" v-model="Lastname"></br>
        <button type="submit" class="btn btn-primary" @click="add()">Add new participant</button>
      </div>
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