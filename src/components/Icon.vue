<template>
    <div id="icon">
        <ul>
            <li>
                <a href="#">
                    <BIconGeoAltFill class="icon"/>
                    <span>Criciúma SC - Brasil</span>
                </a>    
            </li>
            <li>
                <a href="https://www.instagram.com/ramon.souzz/" target="__blank">
                    <BIconInstagram class="icon"/>
                    <span>@ramon.souzz</span>
                </a>    
            </li>
            <li>
                <a href="https://www.facebook.com/ramonsouza.dev/" target="__blank">
                    <BIconFacebook class="icon"/>
                    <span>@ramonsouza.dev</span>
                </a>
            </li>
            <li>
                <a href="https://www.linkedin.com/in/ramonsouzadev/" target="__blank">
                    <BIconLinkedin class="icon"/>
                    <span>@ramonsouzadev</span>
                </a>    
            </li>
            <li>
                <a href="https://github.com/RamonSouzaaa/" target="__blank">
                    <BIconGithub class="icon"/>
                    <span>@RamonSouzaaa</span>
                </a>    
            </li>
        </ul>
    </div>
</template>

<script>
    
    import { 
        BIconGeoAltFill,
        BIconInstagram,
        BIconFacebook,
        BIconLinkedin,
        BIconGithub,
    } from 'bootstrap-icons-vue'
    
    export default {
        name: 'IconComponent',
        components: {
            BIconGeoAltFill,
            BIconInstagram,
            BIconFacebook,
            BIconLinkedin,
            BIconGithub,
        }
    }
</script>

<style scoped>
    #icon {
        display: flex;
        flex-direction: column;
        align-items: center;
        color: var(--color-text);
    }
    
    #icon > ul {
        width: auto;
        list-style-type: none;
        margin: 0;
        padding: 0;
        display: flex;
        flex-direction: column;
        row-gap: 10px;
    }

    #icon > ul > li > a {
        display: flex;
        flex-direction: row;
        column-gap: 5px;
        align-items: center;
        font-family: 'Rubik-Medium';
        text-decoration: none;
        color: var(--color-text);
    }

    #icon > ul > li > .icon{
        width: 25px;
        height: 25px;
    }

    @media screen and (max-width: 840px) {
        #icon > ul {
            display: grid;
            grid-template-areas: "li li";
            row-gap: 10px;
            column-gap:10px;            
        }
    }

    @media screen and (max-width: 396px) {
        #icon > ul {
            display: grid;
            grid-template-areas: "li";
            row-gap: 10px;
            column-gap:10px;            
        }
    }

</style>