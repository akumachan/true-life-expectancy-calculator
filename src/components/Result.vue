<template>
  <div class="result">
    <div id="result" v-if="this.age">
      {{ age }} 才のあなたの寿命は のこり{{ display(age) }}％です。
    </div>
  </div>
</template>

<script>
export default {
  name: 'Result',
  props: {
    age: String
  },
  methods: {
    display: function() {
      const expectancy = 100 - Math.round(100 * Math.log(this.age) / Math.log(80))
      return expectancy >= 0 ? expectancy : 0
    }
  }
}
</script>
