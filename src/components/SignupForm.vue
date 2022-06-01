<template>
  <form>
    <div>
      <label for="username">id: </label>
      <input id="username" type="text" />
    </div>
    <div>
      <label for="password">password: </label>
      <input id="password" type="password" />
    </div>
    <div>
      <label for="nickname">nickname: </label>
      <input id="nickname" type="text" />
    </div>
    <button type="submit">로그인</button>
  </form>
</template>

<script>
export default {
  name: 'SignupForm',
};
</script>

<style scoped></style>
