<template>
  <div className='logo'>      
      <LogoIcon />
      <div className='logo__text'>PNFT Market</div>
    </div>
</template>


<script>
import LogoIcon from '@/components/Icons/LogoIcon.vue';
export default {
  name: 'HeaderBlock', 
  components: { 
        LogoIcon,
     } 
};
</script>


<style lang="scss">
  @import "@/components/Header/Header.scss";
</style>