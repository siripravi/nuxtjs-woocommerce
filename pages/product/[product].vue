<template>
  <div>
  <ProductsSingleProduct :id="route.query.id" :slug="route.params.product" />
</div>
</template>

<script setup>
const route = useRoute();

useHead({
  title: route.params.product,
  titleTemplate: "%s - Nuxt 3 Woocommerce",
  meta: [
    { name: "viewport", content: "width=device-width, initial-scale=1" },
    {
      hid: "description",
      name: "description",
      content: "Nuxt 3 Woocommerce",
    },
  ],
  link: [{ rel: "icon", type: "image/x-icon", href: "/favicon.ico" }],
});
</script>
