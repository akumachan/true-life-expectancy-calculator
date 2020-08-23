<template>
  <div>
    <input
      :type="type"
      :value="age"
      @input="updateValue"
    />
  </div>
</template>

<script>
export default {
  name: 'Input',
  props: {
    age: { type: String },
    type: { type: String }
  },
  methods: {
    updateValue: function() {

    }
  }
}
</script>