<template>
  <div class="App">
      <p>{{name}} - {{age}}</p>
      <button @click="changeName('Zelda')">Change Name</button>
       <button @click="changeAge(30)">Change Age</button>
  </div>

</template>

<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from 'vue'

export default defineComponent({
  name: 'App',
  components: {},
  setup () {
    /*     const state = reactive({
      name: 'Link',
      age: 27 as number | string
    })

    state.name = 'Antonio'

    return { ...toRefs(state) }
*/
    const name = ref('Lins')
    const age = ref<number | string>(25)

    return { name, age }
  },
  methods: {
    changeName (name: string) {
      this.name = name
      return name
    },
    changeAge (age: number |string) {
      this.age = age
      return age
    }
  }
})
</script>

<style>

</style>
