<template>
  <div class="c-navbar">
    <div class="c-container c-container-flex ml-60 mr-60">
      <img src="@/assets/logo.svg" />
      <ul class="c-list">
        <li v-for="(item, index) in menu" :key="index">{{ item.name }}</li>
      </ul>
      <div class="c-form-group">
        <input type="text" placeholder="Search Here" class="c-input" />
        <button class="c-button icon" type="submit">
          <img src="@/assets/img/search.svg" />
        </button>
      </div>
      <div class="ml-10 mr-10">
        <button class="c-button main">Contact Us</button>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class NavBar extends Vue {
  menu = [{ name: "Home" }, { name: "Home" }, { name: "Home" }];
}
</script>
