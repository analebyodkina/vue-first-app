<template>
  <label className="form__field">
      <span className="form__title">{{title}}</span>
      <input         
        className="form__input" 
        :type="inputType"  v-model="inputValue"
        v-bind:placeholder="placeholder"              
      />
      <span className='form__icon'>
        {{icon}}
      </span>
      <span v-on:click="toggleInputType">
        change type
      </span>
      <span v-on:click="clearInputValue">
        clear
      </span>
  </label>                 
       

  
</template>


<script>
// import LogoIcon from '@/components/Icons/LogoIcon.vue';
export default {
  name: 'UiInput', 
  data() {
    return {
      inputType: 'password',
      inputValue: ''
    }
  },
  props: {
    title:{
      type: String,
    },
    icon:{
      type: Object,
    }, 
    placeholder:{
      type: String,
    },       
  },
  methods: {
    toggleInputType() {
      this.inputType = this.inputType === 'text' ? 'password' : 'text';
    },
    clearInputValue() {
      this.inputValue = '';
    }
  } 
  // components: { 
  //       LogoIcon,
  //    } 
};
</script>


<style lang="scss">
  @import "@/components/Ui/Input/Input.scss";
</style>