<template>
  <Page>
     <!-- <card/> -->

    </Page>
</template>

<script>
import card from '../assets/card'
export default {
  props: {
    
  },
  methods: {
    onButtonTap() {
      console.log("Button was pressed");
      this.$navigateBack();
    },
  },
  components: {
    card
  }
}
</script>

<style scoped>
  .card{
    background-color: #FFE601;
    height: 800px;

  }

  .img{
    height: 400px;
    width: 500px;
    margin: 100px
  }
</style>

