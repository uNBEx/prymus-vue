<template>
  <div>
    <h1>Participants list</h1>
      <ol>
        <li :key="string" v-for="string in names">{{string}}</li>
        <!--<button @click="remove()">remove</button>-->
      </ol>
  </div>
</template>

<script>
  export default {
    props: ['names']
  };
</script>