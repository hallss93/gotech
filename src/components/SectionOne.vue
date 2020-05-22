<template>
  <section class="one mt-180">
    <div
      class="c-container c-container-flex wrap align-items-center justify-content-center"
    >
      <h1 class="c-text title capitalize c-animation opacity" id="title">
        We create Simple Solution
      </h1>
      <h2
        class="c-text subtitle capitalize c-animation s2 opacity"
        id="subtitle"
      >
        for your complex task
      </h2>
      <p id="description" class="c-animation s2 opacity">
        Lorem ipsum dolor sit amet, vel accumsan liberavisse ex, ea nec
        elaboraret interpretaris, sed diceret concludaturque no. Verear habemus
        sea ut
      </p>
      <div
        class="ml-10 mr-10 c-container-flex c-animation s2 opacity"
        id="buttons-section-one"
      >
        <button class="c-button main">Our Works</button>
        <button class="c-button empty ml-30">Know More</button>
      </div>
      <img
        src="@/assets/img/group-people.png"
        class="c-image c-animation opacity"
        id="group"
      />
      <img
        src="@/assets/img/floor.svg"
        class="c-image c-animation opacity"
        id="floor"
      />
    </div>
  </section>
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
      const group = document.querySelector("#group") as HTMLCanvasElement;
      const floor = document.querySelector("#floor") as HTMLCanvasElement;
      group.style.opacity = "1";
      floor.style.opacity = "1";

      const background = document.querySelector(".one") as HTMLCanvasElement;
      background.classList.add("background");

      const title = document.querySelector("#title") as HTMLCanvasElement;
      const subtitle = document.querySelector("#subtitle") as HTMLCanvasElement;
      const description = document.querySelector(
        "#description"
      ) as HTMLCanvasElement;
      const buttons = document.querySelector(
        "#buttons-section-one"
      ) as HTMLCanvasElement;

      title.style.opacity = "1";
      setTimeout(() => {
        subtitle.style.opacity = "1";
        setTimeout(() => {
          description.style.opacity = "1";
          buttons.style.opacity = "1";
        }, 500);
      }, 500);
    }, 500);
  }
}
</script>
<style lang="scss">
.one {
  height: 500px;
}
.background {
  background-image: url("./../assets/img/background-one.svg");
}
</style>
