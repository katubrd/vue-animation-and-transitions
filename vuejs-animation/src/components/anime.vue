<template lang="html">
  <div>
    <div>
      <transition name="bounce" appear mode="in-out">
        <div v-if="visible" key="visible">
          <h3 class="text">Woooooo!!!<br>I'm a ghost!!!</h3>
        </div>
        <div v-else="visible" key="invisible">
          <h3 class="text">Woooooo!!!<br>I'm a ghost to!!!</h3>
        </div>
      </transition>
      <button class="toggle-btn" @click="toggle">Toggle</button>
    </div>
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
  .toggle-btn {
    position: absolute;
    top: 25vh;
    right: 48vw;
  }
  .bounce {
    top: 29vh;
  }
  .fade-enter-active, .fade-leave-active {
    transition: opacity .5s, transform .5s;
  }
  .fade-enter, .fade-leave-active {
    opacity: 0;
    transform: translateY(-3vh);
  }
  .bounce-enter-active {
    animation: bounce-in .5s;
  }
  .bounce-leave-active {
    animation: bounce-out .5s;
  }
  @keyframes bounce-in {
    0% {
      transform: scale(0);
    }
    50% {
      transform: scale(1.5);
    }
    100% {
      transfrom: scale(1);
    }
  }
  @keyframes bounce-out {
    0% {
      transform: scale(1.5);
    }
    100% {
      transform: scale(0);
    }
  }


























</style>
