<template>    
    <div className='wrapper'>
        <div className="container">
            <HeaderBlock />
            <LoginBlock />                     
            <FooterBlock />
        </div>
        <div className="image">
        <img src="@/assets/bg-image.png" alt="background" />
        </div> 
    </div>
</template>


<script>
import HeaderBlock from '@/components/Header/HeaderBlock.vue';
import FooterBlock from '@/components/Footer/FooterBlock.vue';
import LoginBlock from '@/components/Login/LoginBlock.vue';


export default {
    name: "HomePage",
    components: { 
        HeaderBlock, 
        FooterBlock, 
        LoginBlock,
     }
};
</script>