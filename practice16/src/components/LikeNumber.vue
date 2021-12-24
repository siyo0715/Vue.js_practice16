<template>
  <div>
    <h2>いいね{{ halfNumber }}</h2>
    <button @click="increment">変化する</button>
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
    props: ["totalNumber"],
    computed:{
      halfNumber(){
        return this.totalNumber / 2
      }
    },
    methods: {
        increment() {
          // this.number += 1;
          this.$emit("my-click", this.totalNumber + 1);
        }
    }
  };
</script>
<style scoped>
  div {
      border: 1px solid red;
    }
</style>