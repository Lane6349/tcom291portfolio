<script setup>
</script>

<script>
import AboutMe from "@/components/AboutMe.vue";
import Contact from "@/components/Contact.vue";
import Skills from "@/components/Skills.vue";
import Home from "@/components/Home.vue";

export default {
  components: {
    Home,
    AboutMe,
  },
  data() {
    return {
      current: 'Home',
    }
  },
  methods: {
    toggleComponent(cName) {
      this.current = cName
    }
  }
}

</script>
<template>
  <header>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.5/dist/css/bootstrap.min.css" rel="stylesheet"
          integrity="sha384-SgOJa3DmI69IUzQ2PVdRZhwQ+dy64/BUtbMJw1MZ8t5HZApcHrRKUc4W0kG879m7" crossorigin="anonymous">
  </header>
  <main>
    <div id="navDiv">
      <div class="d-flex justify-content-between shadow">
        <div>
          <button class="navButton p-3" @click="toggleComponent('Home')">Home</button>
          <button class="navButton p-3" @click="toggleComponent('AboutMe')">About Me</button>
        </div>
        <div>
          <p class="p-3">Last updated on: April 20th, 2025</p>
        </div>
      </div>
    </div>
    <transition name="fade" mode="out-in">
      <component :is="current" />
    </transition>
  </main>
</template>

<style scoped>
#navDiv {
  background-color: rgb(50, 50, 50);
  color: white;
}

.navButton {
  font-size: 1.6rem;
  background-color: transparent;
  border: transparent;
  font-weight: bold;
  color: white;
}

p {
  font-size: 0.8rem;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease-out;
}
</style>
