<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="You did it!" />
      <p>Count: {{ count }}</p>
      <button @click="increment">Increment</button>
      <button @click="decrement">Decrement</button>
    </div>
  </header>

  <!-- <main>
    <TheWelcome />
  </main> -->
</template>

<script>
  export default {
    data() {
      return {
        count: 1
      }
    },

    methods: {
      increment() {
        this.count++
      },
      decrement() {
        this.count--
      }
    }
  }
</script>

<style scoped>
button {
  display: block;
  
}

header {
  line-height: 1.5;
  margin: 0px auto
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    flex-direction: column;
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
    flex-direction: column;
  }
}
</style>
