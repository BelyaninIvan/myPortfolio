<template>
  <button 
    :type="buttonType"
    class="button"
  >
    <slot></slot>
  </button>
</template>
<script>
export default {
  name: 'MyButton',
  props: {
    buttonType: {
      type: String,
      default: null,
    },
  },
  data() {
    return {
        blueTheme: 'button_theme_blue',
        orangeTheme: 'button_theme_orange',
    }
  }
}
</script>
<style scoped>
  .button {
    margin: 0;
    padding: 15px 30px;
    border: 0;
    outline: none;
    cursor: pointer;
    border-radius: 20px;
    background: #223146;

    color: #F4F5EF;
    font-size: 22px;
    font-weight: 700;
    transition: all ease-in .7s;
  }

  .button:hover {
    opacity: .8;
    transform: translateY(-3px);
  }
</style>