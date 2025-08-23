<template>
   <div>
    <h2 class="head ">Skills</h2>
<div class="skills">
  <div class="skill-card">
    HTML
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>
    <div class="box"></div>



    
    
    
    </div>
  <div class="skill-card">CSS

    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
    <div class="box2"></div>
  </div>
  <div class="skill-card">JavaScript

    <div class="box3"></div>
    <div class="box3"></div>
    <div class="box3"></div>
    <div class="box3"></div>
    <div class="box3"></div>
    <div class="box3"></div>
    <div class="box3"></div>
    <div class="box3"></div>
  
  </div>
  <div class="skill-card">React

    <div class="box4"></div>
    <div class="box4"></div>
    <div class="box4"></div>
    <div class="box4"></div>
    <div class="box4"></div>
    <div class="box4"></div>
    <div class="box4"></div>
    <div class="box4"></div>
   
  </div>
  <div class="skill-card">Node.js

    <div class="box5"></div>
    <div class="box5"></div>
    <div class="box5"></div>
    <div class="box5"></div>
    <div class="box5"></div>
    <div class="box5"></div>
    <div class="box5"></div>
    
  </div>
  <div class="skill-card">Python

    <div class="box61"></div>
    
    <div class="box61"></div>
    <div class="box61"></div>
    <div class="box62"></div>
    
    <div class="box62"></div>
    <div class="box62"></div>
  </div>
  <div class="skill-card">C++

    <div class="box7"></div>
    <div class="box7"></div>
    <div class="box7"></div>
    <div class="box7"></div>
    <div class="box7"></div>
    <div class="box7"></div>
    <div class="box7"></div>
    <div class="box7"></div>
   
  </div>
  <div class="skill-card">SQL

    <div class="box8"></div>
    <div class="box8"></div>
    <div class="box8"></div>
    <div class="box8"></div>
    <div class="box8"></div>
    <div class="box8"></div>
    <div class="box8"></div>
    <div class="box8"></div>
    
  </div>
  <div class="skill-card">Git/GitHub

    <div class="box9"></div>
    <div class="box9"></div>
    <div class="box9"></div>
    <div class="box9"></div>
    <div class="box9"></div>
    <div class="box9"></div>
    <div class="box9"></div>
    <div class="box9"></div>
    <div class="box9"></div>
    
  </div>
</div>

   </div>
</template>

<style scoped>
.skills-section {
  height: 100vh;
  width: 230vh;
  background-color: #11071f;
}

.head  {
  font-size: 2.5rem; /* Larger font size for emphasis */
  text-align: center;
  color: #fff;
  padding: 1.5rem 0;
  font-weight: bold;
  letter-spacing: 2px;
  background-color: #11071f;
}
  /* Skills Section */
.skills {
  display: flex;
  flex-wrap: wrap;         /* Wraps skills into multiple rows */
  justify-content: center; /* Centers skills */
  gap: 1rem;               /* Space between cards */
  padding: 2rem;
  background-color: #11071f;
  color: white;
  min-height: 50vh;
}

/* Individual Skill Card */
.skill-card {
  background: #222;
  padding: 1rem 2rem;
  border-radius: 8px;
  font-size: 1rem;
  font-weight: bold;
  color: white;
  text-align: center;
  transition: transform 0.3s ease, background 0.3s ease;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
  cursor: pointer;
}
.box {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: orangered;
}
.box:hover {
  background-color: #f16524;
  transition: 0.2s ease-in;
}
.box2 {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #2162AF;
}
.box2:hover {
  background-color: lightblue;
  transition: 0.2s ease-in;
}
.box3 {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: yellow;
}
.box3:hover {
  background-color: #E4A126;
  transition: 0.2s ease-in;
}
.box4 {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #61DBFB;
}
.box4:hover {
  background-color: #8d8bfc;
  transition: 0.2s ease-in;
}
.box5 {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #7FC728;
}
.box5:hover {
  background-color: darkgreen;
  transition: 0.2s ease-in;
}
.box61 {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #FEC008;
}
.box62 {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #0277bc;
}
.box61:hover {
  background-color: #0277bc;
  transition: 0.2s ease-in;
}
.box62:hover {
  background-color: #FEC008;
  transition: 0.2s ease-in;
}
.box7 {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #00599C;
}
.box7:hover {
  background-color: lightblue;
  transition: 0.2s ease-in;
}
.box8 {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #006EBF;
}
.box8:hover {
  background-color: white;
  transition: 0.2s ease-in;
}
.box9 {
  width: 100%;
  height: 3%;
  margin-top: 1rem;
  border-radius: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
  background-color: #ffff;
}
.box9:hover {
  background-color: #0000;
  transition: 0.2s ease-in;
}


/* Hover Effect */
.skill-card:hover {
  transform: translateY(-5px) scale(1.05);
     /* Purple accent */
}

</style>

<script>
export default {
  data() {
    return {
      isModalVisible: false,
    };
  },
  methods: {
    toggleModal() {
      this.isModalVisible = !this.isModalVisible;
    },
  },
};
</script>

