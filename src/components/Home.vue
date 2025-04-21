<script setup>
import {onBeforeUnmount, onMounted, ref} from "vue";

const x = ref(0)

let hue = Math.floor(Math.random() * 360);
let animation;
let currentHue = 0;
let transition = 0.001;

onMounted(() => {
  const animateRainbow = () => {

    const hueVal = hue - currentHue;

    if (Math.abs(hueVal) < 1) {

      hue = Math.floor(Math.random() * 360);
    } else {

      currentHue += hueVal * transition;
    }

    x.value = currentHue % 360;

    animation = requestAnimationFrame(animateRainbow);
  };

  animateRainbow();
});

onBeforeUnmount(() => {
  cancelAnimationFrame(animation);
});

</script>

<template>
    <div
      :style="{ backgroundColor: `hsl(${x}, 80%, 50%)` }"
      class="movearea d-flex justify-content-center align-items-center"
    >
      <div id="banner">
        <h1>WELCOME</h1>
        <h3>Portfolio made by Lane Thiele.</h3>
      </div>
    </div>
</template>

<style scoped>
.movearea {
  transition: 0.3s background-color ease;
  height: 92.88%;
}

#banner {
  padding-bottom: 15rem;
  text-align: center;
}

h1 {
  font-size: 10rem;
  color: white;
}

h3 {
  color: white;
}

</style>
