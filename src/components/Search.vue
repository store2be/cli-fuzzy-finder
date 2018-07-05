<template>
  <div>
    <input v-model="search" placeholder="Search..." />
    <ul id="example-1">
      <Program v-for="program in filteredPrograms" v-bind:key="program.name" :program="program"></Program>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';
import Program, { CliProgram } from '@/components/Program.vue';

@Component({
  components: { Program },
})
export default class Search extends Vue {
  @Prop(Array) programs: CliProgram[]

  search = ''

  get filteredPrograms() {
    return this.programs.filter(program => program.name.includes(this.search))
  }
}
</script>

<style scoped lang="scss">
</style>
