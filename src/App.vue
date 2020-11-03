<template>
  <div id="app">
    登录
    <form>
      <lable>
        <span>用户名</span>
        <input type="text" v-model="user.username" />
      </lable>
      <lable>
        <span>密码</span>
        <input type="password" v-model="user.password" />
      </lable>
      <button>登录</button>
    </form>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      user: {
        username: "",
        password: "",
      },
    };
  },
  components: {},
};
</script>
