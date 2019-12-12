<template>
    <input :type="type" class="input" :placeholder="placeholder" :value="value" @input="inputbtn">
</template>

<script>
export default {
  props: ['value', 'type', 'placeholder'],
  data () {
    return {

    }
  },
  methods: {
    inputbtn (event) {
      this.$emit('input', event.target.value)
    }
  }
}
</script>

<style lang="less">
.input{
    width: 314*100vw/360;
    height: 40*100vw/360;
    border:none;
    border-bottom: 2px solid #ddd;
    outline: none;
    line-height: 40*100vw/360;
    font-size: 16px;

}
</style>
