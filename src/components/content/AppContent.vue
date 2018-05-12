<template>   
      <div>
            <h3>Minha operadora</h3>
            <forms class="forms"></forms>
            <user-profile class="user_profile"></user-profile>
      </div>   
</template>

<script>
import Forms from "@/components/content/Forms.vue";
import UserProfile from "@/components/content/UserProfile.vue";

export default {
  components: {
    Forms,
    UserProfile
  }
};
</script>

<style scoped>
div {
  padding: 20px 80px;
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 30px 1fr;
  grid-template-areas:
    "header header"
    "forms user_profile";
  grid-gap: 15px;
}

h3 {
  grid-area: header;
   color: #4d4d4d;
   font-weight:normal;
}

.forms {
  grid-area: forms;
}

.user_profile {
  grid-area: user_profile;
  height: 35%;
}

@media (max-width: 640px) {
  h3 {
    text-align: center;
  }
  div {
    padding: 20px 10px;
    grid-template-columns: 1fr;
    grid-template-rows: auto auto auto;
    grid-template-areas:
      "header"
      "user_profile"
      "forms";
    grid-gap: 2px;
  }

  .user_profile {
    height: auto;
  }
}
</style>
