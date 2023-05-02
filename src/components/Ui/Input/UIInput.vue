import { useState } from 'react';
import './Input.scss';

  
function Input(props) {
  const [passwordType, setPasswordType] = useState("password");
  const [inputValue, setInputValue] = useState('');

  const togglePassword = () => {
    if (passwordType === "password" ) {
      setPasswordType("text");
      return;
    }   
    setPasswordType("password");
    console.log(passwordType);

  };


  function handleClearClick() {
    setInputValue('');
  }
  return (    
    <label className="form__field">
        <span className="form__title">{props.title}</span>        

        {props.type === 'password' &&
          <>
            <input type={passwordType}
              value={inputValue}
              onChange={(event) => setInputValue(event.target.value)}      
              className="form__input" 
              placeholder={props.placeholder}
            />
            <span className='form__icon' onClick={togglePassword}>
              {props.icon}
            </span>
          </>          
        }


        {props.type !== 'password' &&
            <>
            <input type={props.type}
              value={inputValue}
              onChange={(event) => setInputValue(event.target.value)}      
              className="form__input" 
              placeholder={props.placeholder}
            />
            <span className='form__icon' onClick={handleClearClick}>
                {props.icon}
            </span>
          </>          
        }  
        
    </label>
    
  )
}

export default Input;

<template>
  <label className="form__field">
      <span className="form__title">{{title}}</span>
      <input 
        type="password"
        className="form__input" 
        v-bind:placeholder="placeholder"          
      />
      <span className='form__icon'>
        {{icon}}
      </span>
  </label>                 
       

  
</template>


<script>
// import LogoIcon from '@/components/Icons/LogoIcon.vue';
export default {
  name: 'UiInput', 
  props: {
    title:{
      type: String,
    },
    // icon:{
    //   type: any,
    // }, 
    placeholder:{
      type: String,
    },       
  } 
  // components: { 
  //       LogoIcon,
  //    } 
};
</script>


<style lang="scss">
  @import "@/components/Ui/Input/Input.scss";
</style>