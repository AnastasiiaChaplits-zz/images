<template>
  <div class="ui secondary pointing menu">
    <a href="/" class="active item"> Image Storage </a>

    <div class="right menu">
      <div v-if="isLoggedIn">

      </div>
      <a href="#" class="ui item" @click="login" v-else> Login </a>
    </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from "vuex";

export default {
  name: "AppHeader",
  computed: mapGetters(["isLoggedIn"]),
  methods: {
    ...mapActions(["login"]),
  },
};
</script>
