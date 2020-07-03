<template>
  <main>
    <header-c :links="links" />
    <router-view class="container px-5 sm:px-20 py-20 flex justify-center" />
  </main>
</template>

<script>
import HeaderC from "@/components/HeaderC";

export default {
  name: "App",
  components: { HeaderC },

  data() {
    return {
      links: [
        {
          title: "Home",
          to: { name: "home" }
        },
        {
          title: "About",
          to: { name: "about" }
        }
      ]
    };
  }
};
</script>

<style></style>
