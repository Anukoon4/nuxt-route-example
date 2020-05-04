<template>
  <div>
    Name: User <br />
    params : {{ JSON.stringify($route.params) }} <br />
    query : {{ JSON.stringify($route.query) }}<br />
    hash : {{ JSON.stringify($route.hash) }}<br />
    <v-btn v-for="i in [1, 2, 3, 4, 5]" :key="i" @click="handelGoto(i)">
      click go to {{ i }}
    </v-btn>
  </div>
</template>

<script>
export default {
  methods: {
    handelGoto(userId) {
      console.log(userId)
      this.$router.push({
        name: 'users-id',
        params: {
          id: userId
        }
      })
    }
  }
}
</script>

<style></style>
