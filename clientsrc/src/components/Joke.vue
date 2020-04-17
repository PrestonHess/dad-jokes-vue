<template>
  <div class="joke col-12">
      <p>{{jokeData.setup}}</p>
      <p>{{jokeData.punchline}}</p>
  </div>
</template>


<script>
export default {
  name: 'joke',
  props: ['jokeData'],
  data(){
    return {}
  },
  computed:{},
  methods:{},
  components:{}
}
</script>


<style scoped>
</style>