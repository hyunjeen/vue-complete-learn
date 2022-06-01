<template>
  <form @submit.prevent="submitform">
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" v-model="username" />
    </div>
    <div>
      <label for="password">password: </label>
      <input id="password" type="password" v-model="password" />
    </div>
    <div>
      <label for="nickname">nickname: </label>
      <input id="nickname" type="text" v-model="nickname" />
    </div>
    <button type="submit">회원가입</button>
    <p>{{ logmsg }}</p>
  </form>
</template>

<script>
import { registerUser } from '@/api';

export default {
  name: 'SignupForm',
  data() {
    return {
      username: '',
      password: '',
      nickname: '',
      logmsg: '',
    };
  },
  methods: {
    async submitform() {
      const userData = {
        username: this.username,
        password: this.password,
        nickname: this.nickname,
      };
      const { data } = await registerUser(userData);
      this.logmsg = `${data.username}님 반갑습니다`;
      this.initForm();
    },
    initForm() {
      this.username = '';
      this.password = '';
      this.nickname = '';
    },
  },
};
</script>

<style scoped></style>
