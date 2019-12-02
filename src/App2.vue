<template>
  <div>  
    <div :class='happy ? "happy" : "sad" '>
        <h1>{{ happy ? "Happy :-)" : "Sad :-(" }}</h1>
    </div>
    <button @click="clicked()">Click me!</button><br>
    
    
  </div>
</template>
 
<script>
    export default {
        data() {
            return {
                happy:true
                }
        },
        methods: {
            clicked() {
                this.happy ? this.happy=false : this.happy=true;
           }
        }
    };
</script>

<style>
.happy{
    color:green;
}
.sad{
    color:grey;
}
</style>