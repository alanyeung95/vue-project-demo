<template>
  <div class="hello">
    <h1>{{ testingMessage }}</h1>
    <h1>{{ msgFromParent }}</h1>
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class DemoComponent extends Vue {
  @Prop() private msgFromParent!: string

  get testingMessage() {
    return 'Hi (computed value) '
  }
}
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
