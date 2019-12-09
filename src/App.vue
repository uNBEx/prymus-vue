<template>
  <div>
    <div>
      <participants-list :names="names"></participants-list>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>Firstname</label>
      <input type="text" v-model="firstname">
      <label>Lastname</label>
      <input type="text" v-model="lastname">
      <button>Add new participant</button>
    </form>
  </div>
</template>

<script>
  import ParticipantsList from "./ParticipantsList.vue";
  export default {
    components: {ParticipantsList},
    data() {
      return {
        names:[],
        firstname:"",
        lastname:"",

      };
    },
    methods: {
      addNewParticipant() {
        if(this.firstname!=""&&this.lastname!=""){
          this.names.push(this.firstname+" "+this.lastname);
          this.firstname="";
          this.lastname="";
        }
      }
    }
  };
</script>