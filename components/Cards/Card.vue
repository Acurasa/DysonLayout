<template>
    <div class="card" :style="cardStyles">
      <slot></slot>
  </div>
</template>
  
<script>
  export default {
    name: 'card-component',
    props: {
      borderRadius: {
        type: Number,
        default: 3
      },
      shadow: {
        type: Object,
        default: () => ({
          top: 0,
          right: 4,
          bottom: 41,
          left: 0,
          color: {
            green: 0,
            red: 0,
            blue: 0,
            alpha: 0.05
          }
        })
      }
    },
    data(){
      return{
        jopa: 2
      }
    },
    computed: {
      cardStyles() {
        return {
          borderRadius: `${this.borderRadius}px`,
          boxShadow: `${this.shadow.top}px ${this.shadow.right}px ${this.shadow.bottom}px ${this.shadow.left}px rgba(${this.shadow.color.red}, ${this.shadow.color.green}, ${this.shadow.color.blue}, ${this.shadow.color.alpha})`
        }
      }
    },
    methods : {

    }
  }
</script>
  
<style scoped>
    .card {
        height: 200px;      
    }
    .offer_card {
        height: 454px;
        width: 325px;
    }
</style>
  