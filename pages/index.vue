<template>
  <section>
    <h1 class="header">5chコピー作ろう！</h1>
    <div class="cards">
      <Card v-for="person in people" :key="person.id" :person="person"></Card>
    </div>
  </section>
</template>

<script lang="ts">
import {
  Component,
  Vue
} from "nuxt-property-decorator"
import { State } from "vuex-class"
import Card from "~/components/Card.vue"

@Component({
  components: {
    Card,
  }
})
export default class extends Vue {
  @State people
}
</script>
<style lang="scss" scoped>
// scssテスト
$size: 500%;
.header {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana,
    sans-serif;
  font-size: $size;
}

.cards {
  display: flex;
  flex-wrap: wrap;
}
</style>
