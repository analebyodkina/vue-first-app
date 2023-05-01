<template>    
    <div className='wrapper'>
        <div className="container">
            <HeaderBlock />
            <LoginBlock /> 
            <UiButton />          
            <FooterBlock />
        </div>
        <!-- <div className="image">
        <img src={mainLogo} alt="background" />
        </div> --> 
    </div>
</template>



<script>
import HeaderBlock from '@/components/Header/HeaderBlock.vue';
import FooterBlock from '@/components/Footer/FooterBlock.vue';
import LoginBlock from '@/components/Login/LoginBlock.vue';
import UiButton from '@/components/Ui/Button/UiButton.vue';


export default {
    name: "HomePage",
    components: { HeaderBlock, FooterBlock, LoginBlock, UiButton }
};
</script>