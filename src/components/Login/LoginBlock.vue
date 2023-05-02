<template>
  <div className="login">
      <h1 className="login__title">NFT Access</h1>
      <div className="login__desc">
        Please fill your detail to access your account.
      </div>

        <form action="get" className="form">
          <UIInput
            :title="'Email'"
            placeholder="debra.holt@example.com"
            type="email"
            :icon="GoogleIcon"
          />
          <UIInput
            :title="'Password'"
            placeholder="••••••••"
            type="password"
            :icon="GoogleIcon"
          />

          <div className="form__row">
            <UiCheckbox :title="'Remember me'" />
            <a href="/">Forgot Password?</a>
          </div>
          <Button type="submit" title="Sign in"></Button>
          
        </form>
        <Button addClass="_secondary"> 
          <span><GoogleIcon /></span>  
          Sign in with Google     
        </Button>
        
        <div className="login__sign-up">
          Don’t have an account?
          <span>            
            <a href="/">Sign up</a>
          </span>
        </div>
      </div>
  
</template>


<script>
import UiCheckbox from '@/components/Ui/Checkbox/UiCheckbox.vue';
// import CloseIcon from '@/components/Icons/CloseIcon.vue'
import UIInput from '../Ui/Input/UIInput.vue';
import GoogleIcon from '../Icons/GoogleIcon.vue';

export default {
  name: 'LoginBlock', 
  components: {
    UiCheckbox,    
    UIInput,
    GoogleIcon,
    // CloseIcon
  },
  data() {
    return {
      // CloseIcon,
      GoogleIcon
    }
  } 
};
</script>

<style lang="scss">
  @import "@/components/Login/Login.scss";
</style>


