<template>
  <div>  
    <h1>Clicked {{ counter }} times</h1>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>
 
<script>
    export default {
        data() {
            return {counter:0}
        },
        methods: {
            iAmClicked() {
                this.counter = this.counter + 1;
            }
        }

    };
</script>
