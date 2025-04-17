<script setup>
</script>

<script>
import AboutMe from "@/components/AboutMe.vue";
import Contact from "@/components/Contact.vue";
import Skills from "@/components/Skills.vue";

export default {
  components: {
    AboutMe,
    Contact,
    Skills
  },
  data() {
    return {
      current: 'AboutMe',
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
    <div id="navDiv">
      <div class="d-flex justify-content-between shadow">
        <div>
          <button class="navButton p-3" @click="toggleComponent('AboutMe')">About Me</button>
          <button class="navButton p-3" @click="toggleComponent('Skills')">Skills and Experience</button>
        </div>
        <div>
          <p class="p-3">Last updated on: {{new Date()}}</p>
        </div>
      </div>
    </div>
  </header>
  <main>
    <component :is="current" />
  </main>
  <footer class="shadow">
    <div class="p-3">
      <p>test</p>
    </div>
  </footer>

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

footer {
  background-color: rgb(50, 50, 50);
  height: 9rem;
}
</style>
