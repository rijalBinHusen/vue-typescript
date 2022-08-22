<template>
  <div class="app">
    <p>{{ jobs[0].location }}</p>
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, toRefs, ref } from 'vue';
import Job from './types/Job'

export default defineComponent({
  name: 'App',
  setup() {
    // const age = ref<number | string>(25)
    // const name = ref('Link');

    // return { age, name }
    
    const jobs = ref<Job[]>([
      { title: 'farm worker', location: 'lon lon ranch', salary: 30000, id: '1' },
      { title: 'quarryman', location: 'death mountain', salary: 40000, id: '2' },
      { title: 'flute player', location: 'the lost woods', salary: 35000, id: '3' },
      { title: 'fisherman', location: 'lake hylia', salary: 21000, id: '4' },
      { title: 'prison guard', location: 'gerudo valley', salary: 32000, id: '5' },
      { title: 'farm worker', location: 'US', salary: 3000, id: '6'}
    ])

    return { jobs }

  },
  // methods: {
  //   changeName(name: string) {
  //     this.name = name
  //     return name
  //   },
  //   changeAge(age: number) {
  //     this.age = age
  //     return age
  //   }
  // }
});
</script>

<style>

</style>
