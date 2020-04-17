<template>
  <div class="about text-center">
    <h1>Welcome {{ profile.name }}</h1>
    <img class="rounded" :src="profile.picture" alt="" />
    <p>{{ profile.email }}</p>
    <MyJoke v-for="MyJoke in MyJokes" :MyJokeData="MyJoke" :key="MyJoke._Id"></MyJoke>
  </div>
</template>

<script>
import MyJoke from "../components/MyJoke.vue"
export default {
  name: "Profile",
  mounted() {
    this.$store.dispatch("getMyJokes");
  },
  computed: {
    profile() {
      return this.$store.state.profile;
    },
    MyJokes() {
      return this.$store.state.myJokes;
    }
  },
  components: {
    MyJoke
  }
};
</script>

<style scoped>
img {
  max-width: 100px;
}
</style>
