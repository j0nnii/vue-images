<template>
  <div class="ui secondary pointing menu">
    <a href="/" class="item active">
      Image Storage
    </a>

    <div class="right menu">
      <div v-if="isLoggedIn" class="horizontal">
        <a class="item">Galleries</a>
        <a class="item">Upload</a>
        <a class="item" href="#" @click="logout">Logout</a>
      </div>
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
  methods: mapActions(['login', 'logout'])
};
</script>

<style scoped>
.horizontal {
  display: flex;
  flex-direction: row;
}
</style>
