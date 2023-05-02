<template>
  <label className="checkbox">
      <input type="checkbox" className="checkbox__input" />
      <!-- <span className="checkbox__checkmark"><CheckIcon /></span> -->
      <span className="checkbox__title">{{ title }}</span>
      
    </label>
</template>


<script>
export default {
  name: 'UiCheckbox',
  props: {
    title: String    
  }  
};
</script>

<style lang="scss">
  @import "@/components/Ui/Checkbox/Checkbox.scss";
</style>
