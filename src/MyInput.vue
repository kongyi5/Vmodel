<template>
  <div class="red wrapper">
    <input :value="value" @input="$emit('input', $event.target.value)" />
  </div>
</template>

<script>
export default {
  name: "MyInput",
  props: {
    value: {
      type: String,
    },
  },
};
</script>

<style scope>
.red {
  background: red;
}
.wrapper {
  display: inline-block;
}
</style>
