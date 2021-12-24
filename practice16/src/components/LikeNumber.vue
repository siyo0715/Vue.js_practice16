<template>
  <div>
    <h2>いいね{{ halfNumber }}</h2>
    <button @click="increment">+1</button>
  </div>
</template>

<script>
  export default {
    // props: {
    //   totalNumber: {
    //     type: Number,
    //     default: 10
    //     },
    //     testProps: {
    //       type: String
    //   }
    // },
    props: ["totalNumber","testProps"],
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