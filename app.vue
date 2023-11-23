<template>
  <div class="font-Poppins">
    <NuxtPage />
  </div>
</template>
<script>
export default {
  setup() {
    const { csrf_token } = useFetch(
      "https://30ed-216-247-59-113.ngrok-free.app/hay/public/api/csrf-token"
    );
  },
  head() {
    meta: [
      {
        name: "csrf-token",
        content: csrf_token,
      },
    ];
  },
};
</script>
