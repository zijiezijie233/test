<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />
      
  </header>
  <!-- <test1 :title="title" :age="age" :names="names"/> -->
  <!-- <test2/> -->
  <test3/>


</template>

<script lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import test1 from './components/test1.vue'
import test2 from './components/test2.vue'
import test3 from './components/test3.vue'
export default {
  name: 'App',
  components: {
    HelloWorld,
    test1,
    test2,
    test3
  },
  data() {
    return {
      title: 'Welcome to Your Vue.js App',
      age: 18,
      names: ['Alice', 'Bob', 'Charlie']
    }
  }
}
</script>



<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>

