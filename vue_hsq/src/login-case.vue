<template>
  <div id="app">
    <div v-if="flag">
      登录
      <el-input v-model="id"></el-input>
      <el-input v-model="password"></el-input>
      <el-button @click="login()">登录</el-button>
    </div>
    <div v-if="!flag">
      <h1>注册</h1>
      <el-input placeholder="姓名" v-model="id"></el-input>
      <el-input placeholder="邮箱" v-model="mailbox"></el-input>
      <el-input placeholder="手机号" v-model="phone"></el-input>
      <el-input placeholder="密码" v-model="password"></el-input>
      <el-input placeholder="请再次输入密码" v-model="password1"></el-input>
      <el-button @click="reg()">注册</el-button>
    </div>
    <el-button @click="change()">切换</el-button>
    
  </div>
</template>

<script>
export default {
  name: "App",
  
 data(){
  return{
    flag:true,
    id:"",
    password:"",
    password1:"",
    mailbox:"",
    phone:""
  }
 },
  methods:{
    change(){
      this.flag =!this.flag
      alert("已切换")
    },
    login(){
      alert("欢迎您"+this.id)
    },
    reg(){
     if (this.password =!this.password1) {
      alert("用户"+this.id+"注册成功")
     } else {
      alert("两次输入不一致 请验证！")
     }
    }
  }
};
</script>

<style>

</style>
