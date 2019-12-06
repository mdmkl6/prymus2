<template>
  <div>

    <div> 
      <participants-list :list="participants"></participants-list>
    </div>

    <div>
      <h3>New participant</h3>
      <new-participant-form @added="addNewParticipant($event)"></new-participant-form>
    </div>

  </div>
</template>
 
<script>
  import ParticipantsList from "./ParticipantsList.vue";
  import NewParticipantForm from "./NewParticipantForm.vue";
  export default {
    components: {ParticipantsList,NewParticipantForm},
    data() 
    {
      return {participants: []}
    },
      methods: 
    {
      addNewParticipant(newParticipant) {
        this.participants.push(newParticipant);
      }
    }
  };
</script>