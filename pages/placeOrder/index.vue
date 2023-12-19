<template>
<div>
    <div class="container">
    <h1><span><i class="ri-checkbox-fill"></i></span>Order-
successful!</h1>
    <h2>Thank you!</h2>
    <p>A Order-confirmation has been sent to your email,<br>
        Purchase more for additional shopping benefits!
    </p>
    <button @click="goBackToHomePage">Continue-Shopping</button>
</div>
</div>
</template>

<script setup>
import { useRouter } from "vue-router";
const router = useRouter();

const goBackToHomePage = () => {
  router.push("/");
  return;
};
</script>