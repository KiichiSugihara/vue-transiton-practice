<template>
  <div>
    <button @click="isShown =!isShown">表示の切り替え</button>
    <transition>
      <p v-show="isShown">
        <slot>HELOO!!!</slot>
      </p>
    </transition>
  </div>
</template>

<script>
export default {
  name: "TButton",
  data: function() {
    return {
      isShown: false
    };
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.v-enter-active,
.v-leave-active {
  transition: opacity 500ms ease-out;
}

.v-enter {
  opacity: 0;
}

.v-enter-to {
  opacity: 1;
}

.v-leave {
  opacity: 0;
}

.v-leave-to {
  opacity: 1;
}
</style>
