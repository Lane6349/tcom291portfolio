<script setup>

</script>

<template>
  <div class="p-3 row justify-content-around">
    <div class="col-4">
      <div class="shadow p-2">
        <h3>Lane Thiele</h3>
        <h4 class="pt-3">Contact Information:</h4>
        <p class="pt-2">Linked In: link</p>
        <p>Email: lane.thiele@outlook.com</p>
        <p>Phone Number: 431-345-0227</p>
        <h4>Career Goals:</h4>
        <p class="goals">
          I would love to work with others on a team developing a massive project.
          The process of building a project with others is one of the most fulfilling events to participate in.
          This could involve working on a webapp, desktop application, or potentially even
          someday video game development. I also want to work within the networking industry someday,
          whether that would be replacing / installing networking technology or maintaining a
          server.
        </p>
        <h4>Other Skills:</h4>
        <p class="goals">Java, .Net, C, Entra/Azure, Database management, Networking, Docker.</p>
      </div>
    </div>
    <div class="col">
      <div class="shadow p-2">
        <h3>Skills and Experience</h3>
        <div class="row">
          <div class="col-6 pt-3">
            <h4>Strong skills in React and NextJS</h4>
            <img src="/thugcas.png" alt=""/>
          </div>
          <div class="col-6 pt-3">
            <h4>Good understanding of Vue</h4>
            <img src="/thugcas.png" alt=""/>
          </div>
          <div class="col-6 pt-3 pb-3">
            <h4>Knowledgeable in User Experience</h4>
            <img src="/craig.png" alt=""/>
          </div>
          <div class="col-6 pt-3">
            <h4>Handlebars and TypeORM</h4>
            <img src="/catgallery.png" alt=""/>
          </div>
        </div>
        </div>
      </div>
    </div>
</template>

<style scoped>
.shadow {
  height: 100%;
}

.goals {
  padding-right: 50px;
}

.row {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  text-align: left;
}
.col-6 {
  display: flex;
  flex-direction: column;
  align-items: center;
}

img {
  width: 90%;
  border: 3px solid black;
}

p, h4, h3 {
  padding-left: 5px;
  padding-right: 5px;
}

p {
  font-size: 1.35rem;
}
</style>