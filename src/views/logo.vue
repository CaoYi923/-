<template>
  <div class="box">
    <div id="app">
      <div class="container">
        <div class="close">
          <span class="iconfont iconicon-test"></span>
        </div>
        <div class="logo">
          <span class="iconfont iconnew"></span>
        </div>
        <div class="inputs">
          <!-- <input data-v-744880be placeholder="请输入手机号" class="input" /> -->
          <!-- <input data-v-744880be placeholder="密码" class="input" type="password" /> -->
          <myinput type="text" placeholder="请输入手机号" :value="users.username" @input="input" :rules='/^1(3|5|6|7|8|9)\d{9}/'></myinput>
          <myinput type="password" placeholder="请输入密码" :value="users.userpwd" v-model="users.password"></myinput>
        </div>
        <p class="tips">
          没有账号？
          <a href="#/register" class>去注册</a>
        </p>
        <!-- <div data-v-4bc01e24 class="button">登录按钮</div> -->
        <mybutton @click="btn"></mybutton>
      </div>
    </div>
  </div>
</template>

<script>
import mybutton from '../components/mybutton'
import myinput from '../components/myimput'
export default {

  data () {
    return {
      users: {
        username: 'jack',
        password: '123456'
      }
    }
  },
  components: {
    mybutton, myinput
  },
  methods: {
    btn (data) {
      console.log('1111', this.users)
    },
    input (data) {
      console.log('222222', data)
      this.users.username = data
      // this.user.userpwd = data
    }
  }
}
</script>

<style lang="less" scoped>
.container {
  padding: 20px;
}

.close {
  span {
    font-size: 27 / 360 * 100vw;
  }
}

.logo {
  display: flex;
  justify-content: center;

  span {
    display: block;
    font-size: 126 / 360 * 100vw;
    color: #d81e06;
  }
}

.inputs {
  input {
    margin-bottom: 20px;
  }
}

.tips {
  text-align: right;
  margin-bottom: 20px;

  a {
    color: #3385ff;
  }
}
</style>
