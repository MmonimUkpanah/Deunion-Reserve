<template>
    <div>
        <footer>
            <div class="f1">
                <font-awesome-icon class="ico" :icon="['fab', 'facebook']"/>
                <font-awesome-icon class="ico" :icon="['fab', 'instagram']"/>
                <font-awesome-icon class="ico" :icon="['fab', 'twitter']"/>
                <font-awesome-icon class="ico" :icon="['fab', 'linkedin']"/>
            </div>
            <div class="f2">
                <p>Imprint <span class="space">|</span> Legal resources <span class="space">|</span> Data protection <span class="space">|</span> Accessibility <span class="space">|</span> Sitemap <span class="space">|</span> Contact </p>
                <p>Copyright &#169; 2021 Deutsche Bank, AG, Frankfurt am Main</p>
            </div>
        </footer>
    </div>
</template>
<style scoped>
    footer{
        margin-top: 4rem;
        background-color: #f3f4f5;
    }
    .f1{
        margin-left: 5%;
        margin-right: 5%;
        padding-top: 3rem;
    }
    .ico{
        font-size: 40px;
        margin-right: 2rem;
        color: #0272A2;
    }
    .f2{
        margin-left: 5%;
        margin-right: 5%;
        padding-top: 1rem;
        padding-bottom: 4rem;
    }
    .f2 p{
        font-size: 17px;
    }
    .space{
        margin-left: 10px;
        margin-right: 10px;
    }
    @media(max-width:567px){
        .ico{
        font-size: 30px;
        margin-right: 1rem;
        color: blue;
    }
    }


</style>