<template >
  <a 
    :href="addr"
    class="link"
    target="_blank"
  >
    <slot></slot>
  </a>
</template>
<script>
export default {
  name: 'MyLinkBtn',
  props: {
    addr: {
      type: String,
      required: true
    }
  }
}
</script>
<style scoped>
  .link {
    margin: 0;
    padding: 15px 30px;
    text-decoration: none;
    cursor: pointer;
    border-radius: 20px;
    background: #F28E14;

    color: #F4F5EF;
    font-size: 14px;
    font-weight: 700;
    transition: all ease-in .7s;
  }

  .link:hover {
    opacity: .8;
    transform: translateY(-3px);
  }
</style>