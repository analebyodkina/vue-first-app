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
            :icon="CloseIcon"
          />
          <!-- <Input
            title="Password"
            placeholder="••••••••"
            type="password"
            icon={<ClosedEyeIcon />}
          /> -->

          <div className="form__row">
            <UiCheckbox :title="'Remember me'" />
            <a href="/">Forgot Password?</a>
          </div>
          <Button type="submit" title="Sign in"></Button>
          
        </form>
        <!-- <Button linkTo="/" title="Sign in with Google" addClass="_secondary" icon={<GoogleIcon />}>        
        </Button> -->
        
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
// import CloseIcon from '@/components/Icons/CloseIcon.vue';
import UIInput from '../Ui/Input/UIInput.vue';

export default {
  name: 'LoginBlock', 
  components: {
    UiCheckbox,
    // CloseIcon,
    UIInput
} 
};
</script>

<style lang="scss">
  @import "@/components/Login/Login.scss";
</style>


