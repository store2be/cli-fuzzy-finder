<template>
<div>
  <h3>{{ program.name }}</h3>
  <p>{{ program.description }}</p>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator';

interface CliProgram {
  name: string
  website_url: string
  github_url: string
  language: string
  description: string
}

@Component
export default class Program extends Vue {
  @Prop() private program: CliProgram;
}
</script>

<style scoped lang="scss">
</style>
