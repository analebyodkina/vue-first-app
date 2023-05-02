<template>
  <button className="btn">
      <span className="btn__icon">{{ btnIcon }}</span>       
      <span className="btn__text">{{ title }}</span>      
    </button>
</template>


<script>
export default {
  name: 'UiButton', 
  props: {
    title: {
      type:String
    },
    btnIcon: {
      type: Object
    }   
  }  
};
</script>

<style lang="scss">
  @import "@/components/Ui/Button/Button.scss";
</style>