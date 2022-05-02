<template>
    <div id="profile-pic">
        <img src="../assets/profile-pic.webp" alt="Profile-Pic">
        <h2>Ramon de Souza</h2>
        <h4>Desenvolvedor de Software</h4>
    </div>
</template>
    
<script>
    export default {
        name: 'ProfilePicComponent'
    };
</script>

<style scoped>
    #profile-pic{
        color: var(--color-light);
        width: auto;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    #profile-pic > img {
        width: 172px;
        height: 169px;
        border-radius: 100%;
    }

    #profile-pic > h2 {
        font-family: "Rubik-SemiBold";
        color: var(--color-text);
    }
    
    #profile-pic > h4 {
        font-family: "Rubik-Regular";
        margin-top:-15px;
        color: var(--color-text);
    }

</style>
