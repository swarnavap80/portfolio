<template>
  <div>
    <NavBar />
    <div class="container1">
      <h4>Hello! I am <span>Swarnava Paul</span></h4>
      <div class="arrow">
        <img src="../src/assets/arrow_white-removebg-preview.png" alt="" />
      </div>
      <div class="profile-img">
        <img src="../src/assets/profile-img.png" alt="" />
      </div>
      <div class="content">
        <p>A Programmer who</p>
        <h2>Judges a book</h2>
        <h2>by its <span id="spn1">cover</span><span id="spn2">...</span></h2>
        <span id="spn3"
          ><p>
            because if the cover does not impress you what else can ?
          </p></span
        >
      </div>
      <div class="content-2">
        <h2>I'm a final year B.tech Student 🧑‍🎓.</h2>
        <h3>Full Stack Developer 💻</h3>
      </div>
      <div class="content-3">
        <p>
          A self-taught software Engineer designer, functioning in the industry
          for 1+ years now.I make meaningful and delightful digital products
          that create an equilibriumbetween user needs and business goals.
        </p>
      </div>
    </div>
    <div class="container-2">
      <div class="content-4">
        <h2>Work Experience</h2>
        <Box4 />

        <div class="button1">
          <a href="/public/Swarnava_paul_079.pdf"><button>Get My CV</button></a>
        </div>
      </div>
      <div class="content-5">
        <h3>I'm looking to join a <span>cross functional</span> team</h3>
        <p>
          that values improving people's life through acessible
          program/code/design
        </p>
      </div>
    </div>
    <skills />
    <projects />
    <contacts />
  </div>
</template>

<script setup>
import NavBar from "./components/NavBar.vue";
import skills from "./components/skills.vue";
import Box4 from "./components/Box4.vue";
import projects from "./components/projects.vue";
import contacts from "./components/contacts.vue";
</script>

<style scoped>
.container1 {
  height: 100%;
  width: 100vw;
  background-color: #11071f;

  overflow: hidden;
  color: #fff;
}
.container1 h4 {
  margin-left: 46%;
  margin-top: 6%;
  font-family: "Roboto Mono", monospace;
}
.container1 span {
  color: #693b93;
  font-weight: 600;
}
.arrow img {
  height: 12vh;
  width: 12vw;
  transform: rotate(180deg);
  margin-left: 35%;
  margin-top: -2rem;
}
.profile-img img {
  height: 13%;
  width: 13%;
  margin-left: 24%;
}
.content {
  margin-left: 40%;
  margin-top: -10%;
  font-size: 20px;
  font-family: "Roboto Mono", monospace;
}
.content p {
  margin-left: 0.5rem;
}
#spn2 {
  color: #fff;
  margin-left: 0.5rem;
}
#spn3 p {
  color: #fff;
  font-size: 12px;
  margin-top: 0.3rem;
  margin-left: -0.01rem;
}
.content-2 {
  height: 20%;
  width: 100%;
  margin-left: 26%;
  margin-top: 10%;
  line-height: 2;
  font-family: "Roboto Mono", monospace;
}
.content-3 {
  margin-left: 26%;
  font-family: "Roboto Mono", monospace;
  height: 20%;
}
.content-3 p {
  width: 60%;
  margin-top: 5%;
}
.container-2 {
  height: 100%;
  width: 100%;
  background-color: #11071f;
  color: #fff;
  overflow: hidden;
}
.content-4 {
  height: 150%;
  width: 100%;
}
.content-4 h2 {
  margin-left: 45%;
  margin-top: 10%;
  font-family: "Roboto Mono", monospace;
}

.button1 button {
  margin-top: 4%;
  margin-left: 46.5%;
  height: 6vh;
  width: 8vw;
  border-radius: 30px;
  font-family: "Roboto Mono", monospace;
  background-image: linear-gradient(#844ed1, #311755, #250f42);
  color: white;
  border: none;
  cursor: pointer;
}
.content-5 h3 {
  font-family: "Roboto Mono", monospace;
  margin-top: 5rem;
  margin-left: 35%;
}
.content-5 p {
  font-family: "Roboto Mono", monospace;
  margin-top: 0.6em;
  margin-left: 27.5%;
  margin-bottom: 10%;
}
</style>
