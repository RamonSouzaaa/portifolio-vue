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
        border:1px solid white;
    }
    
    #icon > ul {
        list-style-type: none;
        margin: 0;
        padding: 0;
        color:white;
    }

    #icon > ul > li > .icon{
        width: 25px;
        height: 25px;
    }
</style>