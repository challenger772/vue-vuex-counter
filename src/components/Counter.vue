<template>
  <div>
    <h2>Welcome to Counter</h2>
    <div><h3>Counter: </h3>{{ counter }}</div>
    <button @click="incrementCounter">increment counter</button>
  </div>
</template>

<script>
export default {
  methods: {
    incrementCounter () {
      this.$store.dispatch('incrementAction', 1)
    }
  },

  computed: {
    counter () {
      return this.$store.getters.counter
    }
  }
}
</script>