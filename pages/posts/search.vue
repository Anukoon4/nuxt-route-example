<template>
  <div>
    Name: Posts-postId <br />
    params : {{ JSON.stringify($route.params) }} <br />
    query : {{ JSON.stringify($route.query) }}<br />
    hash : {{ JSON.stringify($route.hash) }}<br />
    <v-text-field v-model="query" label="Regular"></v-text-field>
    <v-btn @click="handelSearch">Search</v-btn>
  </div>
</template>

<script>
export default {
  data() {
    return {
      query: ''
    }
  },
  methods: {
    handelSearch() {
      console.log('click')
      this.$router.push({
        name: 'posts-search',
        query: {
          name: this.query
        }
      })
    }
  }
}
</script>

<style></style>
