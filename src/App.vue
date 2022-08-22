<template>
  <div class="app">
    <p>{{ name }} - {{ age }}</p>
    <button @click="changeName('tests')">Change name</button>
    <button @click="changeAge(30)">Change age</button>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs } from 'vue';

export default defineComponent({
  name: 'App',
  setup() {

    const state = reactive({
      name: 'link',
      age: 25 as number,
    })

    return { ...toRefs(state)}
  },
  methods: {
    changeName(name: string) {
      this.name = name
      return name
    },
    changeAge(age: number) {
      this.age = age
      return age
    }
  }
});
</script>

<style>

</style>
