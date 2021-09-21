<template>
  <div class='modal'>
    <div class='overlay' @click="emit('closeModal')"></div>
    <div class='modal-card'>
      <slot/>
    </div>
  </div>
</template>

<script>
export default {
  setup(props, {emit}) {
    let onKeyDown = (event) => {
      console.log(event.key)
    }
    window.addEventListener('keydown', onKeyDown)
    return {
      emit
    }
  }
}
</script>

<style scoped>

</style>
