<template>
  <div>
    <h2>いいね{{ halfNumber }}</h2>
    <button @click="increment">+1</button>
  </div>
</template>

<script>
  export default {
    props: {
      totalNumbe: Number
    },
    computed:{
      halfNumber(){
        return this.totalNumber / 2
      }
    },
    methods: {
        increment(){
          this.number += 1;
        }
    }
  };
</script>
<style scoped>
  div {
      border: 1px solid red;
    }
</style>