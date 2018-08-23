<template>
  <div class="ui secondary pointing menu">
    <a href="/" class="item active">
      Image Storage
    </a>

    <div class="right menu">
      <a class="ui item" href="#" v-if="isLoggedIn">
        Logout
      </a>
      <a class="ui item" href="#" @click="login" v-else>
        Login
      </a>

    </div>
  </div>
</template>

<script>
import { mapActions, mapGetters } from 'vuex';

export default {
  name: 'AppHeader',
  computed: mapGetters(['isLoggedIn']),
  methods: mapActions(['login'])
};
</script>
