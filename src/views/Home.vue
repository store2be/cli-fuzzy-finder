<template>
  <div>
    <Search :programs="programs" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import Search from '@/components/Search.vue';
import Program from '@/components/Program.vue';

@Component({
  components: {
    Program,
    Search,
  },
})
export default class Home extends Vue {
  programs = [{
    name: 'ponysay',
    website_url: 'http://erkin.co/ponysay/',
    github_url: 'https://github.com/erkin/ponysay',
    language: 'The language of the ponies',
    description: 'Today your terminal, tomorrow the world!',
  }, {
    name: 'sl',
    github_url: 'https://github.com/mtoyoda/sl',
    website_url: 'https://github.com/mtoyoda/sl',
    language: 'C',
    description: 'SL (Steam Locomotive) runs across your terminal when you type "sl" as you meant to type "ls". It\'s just a joke command, and not useful at all.',
  }]
}
</script>
