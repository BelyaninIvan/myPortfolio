<template>
  <button 
    :type="buttonType"
    :projectItem="projectItem"
    :class="[projectItem ? orangeTheme : blueTheme]"
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
    projectItem: {
      type: Boolean,
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
    border-radius: 20px;

    color: #F4F5EF;
    font-size: 22px;
    font-weight: 700;
    transition: all ease-in .7s;
  }

  .button_theme_blue {
    background: #223146;
  }

  .button_theme_orange {
    background: #F28E14;
  }

  .button:hover {
    opacity: .6;
    transform: translateY(-3px);
  }
</style>