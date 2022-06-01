<template>
  <div>
    <h1>회원가입페이지</h1>
    <signup-form></signup-form>
  </div>
</template>

<script>
import SignupForm from '@/components/SignupForm';

export default {
  name: 'SignupPage',
  components: { SignupForm },
};
</script>

<style scoped></style>
