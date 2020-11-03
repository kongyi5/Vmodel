<template>
  <div id="app">
    {{ user }}
    <hr />
    登录
    <form @submit.prevent="onSubmit">
      <lable>
        <span>用户名</span>
        <input
          type="text"
          :value="user.username"
          @input="user.username = $event.target.value"
        />
      </lable>
      <lable>
        <span>密码</span>
        <MyInput :value="user.password" @input="user.password = $event" />
      </lable>
      <button>登录</button>
    </form>
  </div>
</template>

<script>
import MyInput from "./MyInput.vue";
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
  methods: {
    onSubmit() {
      console.log(this.user);
    },
  },
  components: {
    MyInput,
  },
};
</script>
