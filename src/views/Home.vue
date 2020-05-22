<template>
  <div class="home">
    <NavBar msg="Welcome to Your Vue.js App" />
    <div class="mt-105">
      <SectionOne></SectionOne>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import NavBar from "@/components/NavBar.vue";
import SectionOne from "@/components/SectionOne.vue";

export default {
  name: "Home",
  components: {
    NavBar,
    SectionOne
  }
};
</script>
