<template>
  <div class="c-navbar">
    <div class="c-container c-container-flex ml-60 mr-60">
      <img src="@/assets/logo.svg" />
      <ul class="c-list">
        <li v-for="(item, index) in menu" :key="index">
          <p v-bind:class="{ active: item.active }">{{ item.name }}</p>
          <p v-if="item.active" class="c-dot"></p>
        </li>
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

@Component({})
export default class NavBar extends Vue {
  menu = [
    { name: "Home", active: true },
    { name: "About", active: false },
    { name: "Product", active: false },
    { name: "Career", active: false },
    { name: "Blog", active: false }
  ];
  created() {
    setTimeout(() => {
      const element = document.querySelector(".c-navbar") as HTMLCanvasElement;
      element.style.top = "0px";
      setTimeout(() => {
        element.style.opacity = "1";
      }, 300);
    }, 500);
  }
}
</script>
