<template>
  <div id="app">
    <h1 id="header">体感寿命計算機</h1>
    <div id="description">
      寿命を80才として<a href="https://ja.wikipedia.org/wiki/%E3%82%B8%E3%83%A3%E3%83%8D%E3%83%BC%E3%81%AE%E6%B3%95%E5%89%87">ジャネーの法則</a>を用いて体感寿命を計算します。計算式が合っているかはわかりません。
    </div>
    <Result :age="age"></Result>
    <Input :age="age" @input="this.age = $event.target.value" type="number" />
    <!-- <Input v-model="age" /> -->
  </div>
</template>

<script>
import Result from './components/Result.vue'
import Input from './components/Input.vue'

export default {
  name: 'App',
  data () {
    return {
      age: '',
    }
  },
  components: {
    Result,
    Input
  },
}
</script>