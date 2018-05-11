<template>
    <div>
            <h3>Minha operadora</h3>
            <forms class="forms"></forms>
            <user-profile class="user_profile"></user-profile>

    </div>
</template>

<script>

import Forms from "@/components/content/Forms.vue";
import UserProfile from "@/components/content/UserProfile.vue"

export default {
    components:{
        Forms,
        UserProfile
    }
};
</script>


<style scoped>

div{
    padding: 20px 80px;
    display: grid;
    grid-template-columns: 800px 1fr;
    grid-template-rows: 30px 1fr;
    grid-template-areas: 
    "header header"
    "forms user_profile";
    grid-gap: 15px;    
}

h3{
    grid-area: header
}

.forms{
    grid-area: forms;
}

.user_profile{
    grid-area: user_profile;
}

</style>
