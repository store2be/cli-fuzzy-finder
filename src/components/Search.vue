<template>
  <div>
    <input v-model="search" placeholder="Search..." />
    <ul id="example-1">
      <li v-for="program in programs">
        <Program program={programs} />
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Program from '@/components/Program.vue';

@Component({
  components: { Program },
})
export default class Search extends Vue {
  search = ''
}
</script>

<style scoped lang="scss">
</style>
