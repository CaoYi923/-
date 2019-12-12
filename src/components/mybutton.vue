<template>
    <div class="btn" @click="mybtn">
        登陆
    </div>
</template>

<script>
export default {
  data () {
    return {

    }
  },
  methods: {
    mybtn (event) {
      this.$emit('click', event)
    }
  }
}
</script>

<style lang="less" scoped>
.btn{
    width: 314*100vw/360;
    height: 48*100vw/360;
    background-color: #cb3100;
    color: #fff;
    font-size: 18px;
    border-radius: 48*100vw/360;
    text-align: center;
    line-height:48*100vw/360;

}
</style>
