<template>
    <div id="icon">
        <ul>
            <li>
                <BIconGeoAltFill class="icon"/>
                <span>Criciuma SC - Brasil</span>
            </li>
            <li>
                <BIconInstagram class="icon"/>
                <span>@ramon.souzz</span>
            </li>
            <li>
                <BIconFacebook class="icon"/>
                <span>@ramonsouza.dev</span>
            </li>
            <li>
                <BIconLinkedin class="icon"/>
                <span>@ramonsouzadev</span>
            </li>
            <li>
                <BIconGithub class="icon"/>
                <span>@RamonSouzaaa</span>
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

    #icon > ul > li {
        display: inline;
        display: flex;
        flex-direction: row;
        column-gap: 5px;
        align-items: center;
        font-family: 'Rubik-Medium';
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