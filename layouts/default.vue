<template>
  <v-app dark>
    <v-main>
      <Navbar />
      <v-container>
        <Nuxt />
      </v-container>
      <Footer />
    </v-main>
  </v-app>
</template>

<script>
export default {
  name: "DefaultLayout",
  data: () => ({}),
};
</script>
