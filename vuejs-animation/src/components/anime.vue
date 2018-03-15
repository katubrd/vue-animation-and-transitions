<template lang="html">
  <div>
    <div v-if="visible">
      <h3 class="text">Woooooo!!!<br>I'm a ghost!!!</h3>
    </div>
    <button @click="toggle">Toggle</button>
  </div>
</template>

<script>
export default {
  data () {
    return {
      visible: true
    }
  },
  methods: {
    toggle: function() {
      this.visible = !this.visible
    }
  }
}
</script>

<style lang="css">
</style>
