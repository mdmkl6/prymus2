<template>
  <div>  
    <div>
      <h3>New participant</h3>
      <new-participant-form @added="addNewParticipant($event)"></new-participant-form>
    </div>
    <div> 
      <participants-list :list="participants"></participants-list>
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
      addNewParticipant(participant) {
        this.participants.push(addNewParticipant.Firstname+" "+addNewParticipant.Lastname);
      }
    }
  };
</script>