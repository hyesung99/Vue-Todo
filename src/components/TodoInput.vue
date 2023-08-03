<template>
  <input
    ref="input"
    @change="$emit('change', $event.target.value), setEmpty()"
    @keydown.enter="$emit('submit', $event.target.value)"
    placeholder="할 일을 입력하세요"
  />
  <button @click="$emit('submit')">등록</button>
</template>
<script>
export default {
  props: {},
  data() {
    return {}
  },
  methods: {
    setEmpty() {
      this.$refs.input.value = ''
    },
  },
  emits: ['submit', 'change'],
}
</script>
