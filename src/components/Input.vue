<template>
  <div>
    私は現在
    <input
      :type="type"
      :value="age"
    />
    才です。
  </div>
</template>

<script>
export default {
  name: 'Input',
  props: {
    age: { type: String },
    type: { type: String }
  },
}
</script>