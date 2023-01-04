<template lang="pug">
button.button(:style=styles)
  span
  slot
</template>

<!--<template>-->
<!--  <button :style=styles class="button">-->
<!--    <span><slot></slot></span>-->
<!--  </button>-->
<!--</template>-->

<script>
export default {
  name: "ButtonPrimary",

  props: {
    background: String,
    color: String,
  },

  setup(props) {
    const styles = {
      background: `#${props.background}`,
      color: `#${props.color}`,
    }

    return {
      styles
    }
  },
}
</script>

<style scoped lang="scss">

.button {
  font-family: 'Dela Gothic One', sans-serif;
  font-style: normal;
  font-weight: 800;
  font-size: 14px;
  line-height: 100%;
  letter-spacing: 0.02em;
  text-transform: uppercase;
  color: #171717;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 16px 32px;
  gap: 10px;
  background: transparent;
  border: 2px solid #171717;
  border-radius: 80px;
}

</style>