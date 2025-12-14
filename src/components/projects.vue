


<template>
  <div>
    <!-- Heading -->
    <h2 class="head">Projects</h2>

    <!-- Projects Container -->
    <div class="projects">
      <div
        v-for="(project, index) in projects"
        :key="index"
        class="project-container"
        :class="{ animate: animationTriggered }"
      >
        <div class="details">
          <p>Featured Project</p>
          <h1>{{ project.title }}</h1>
        </div>
        <div class="desc">
          {{ project.description }}
        </div>
        <div class="project-img">
        <img :src="project.image" alt="Project image">
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Projects",
  data() {
    return {
      projects: [
        {
          title: "Employee management system",
          description:
            "This project is built using React js, Local storage and Context Api. ",
            image: '/employee.png'
        },
        {
          title: " Project 2",
          description:
            "Book mark app dyanmic page built using supabase vue and node js",
            image: '/src/assets/3d-illustration-bookmark-icon-260nw-2696868009.webp'
        },
        {
          title: " Project 3",
          description:
            "Ai Powered PPT Maker built using Gemini Api , ppt libray python and streamlit",
            image: '/src/assets/ppt-maker.png'
        },
      ],
      animationTriggered: false,
    };
  },
  mounted() {
    this.triggerAnimations();
  },
  methods: {
    triggerAnimations() {
      // Simulate triggering animations on mount
      setTimeout(() => {
        this.animationTriggered = true;
      }, 500); // Delay to simulate scrolling or element loading
    },
  },
};
</script>

<style scoped>
.head {
  font-size: 2.5rem; /* Larger font size for emphasis */
  text-align: center;
  color: #fff;
  padding: 1.5rem 0;
  font-weight: bold;
  letter-spacing: 2px;
  background-color: #11071f;
}

/* Projects Container - Row Layout */
.projects {
  display: flex;
  justify-content: center;   /* Centers all project cards horizontally */
  align-items: center;       /* Centers vertically if needed */
  flex-wrap: wrap;           /* Wrap cards to new row if space runs out */
  gap: 2rem;                 /* Space between cards */
  padding: 2rem;
  background-color: #11071f; /* Section background */
  color: white;
  min-height: 100vh;  
}

/* Individual Project Container */
.project-container {
  display: flex;
  flex-direction: column;    /* Stack image, title, desc vertically */
  align-items: center;       /* Center content inside */
  background-color: #222;
  padding: 1rem;
  border-radius: 8px;
  width: 350px;       /* Fixed width for all cards */
  height: 450px;      /* Fixed height for consistency */
  color: white;
  opacity: 0;         /* Initial state for animation */
  transform: translateY(50px);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
}

.project-container.animate {
  opacity: 1;
  transform: translateY(0);
}

/* Project Image */
.project-img {
  width: 100%;
  height: 220px;   /* Bigger image */
  overflow: hidden;
  border-radius: 8px;
  background-color: black; /* fallback */
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1rem;
}

.project-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;   /* Keeps image proportional */
  border-radius: 8px;
}

/* Project Details */
.details {
  text-align: center;
  margin-bottom: 0.5rem;
}

.details p {
  font-size: 14px;
  margin: 0;
  opacity: 0.8;
}

.details h1 {
  font-size: 20px;
  margin: 0.5rem 0;
}

/* Project Description */
.desc {
  flex-grow: 1;                /* Pushes to take remaining space */
  background-color: #fff;
  color: black;
  padding: 0.8rem;
  border-radius: 8px;
  font-size: 14px;
  text-align: center;
  overflow: hidden;
}

/* Fixed Project Image Styling */
.project-img {
 grid-column: 1 / 3;   /* Make image span across both columns */
  width: 100%;          /* Full width of card */
  height: 250px;
  margin-top: 20px;        /* Increase height */
  overflow: hidden;
  border-radius: 8px;
  background-color: black; /* fallback background */
  display: flex;
  align-items: center;
  justify-content: center;
}

.project-img img {
    width: 100%;
  height: 100%;
  object-fit: fill;    /* Makes sure image fills nicely without distortion */
  border-radius: 8px;
}

/* CSS Animation */
@keyframes fade-slide {
  from {
    opacity: 0;
    transform: translateY(50px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.project-container.animate {
  animation: fade-slide 0.8s ease-out forwards;
}

/* Responsive Styles */
@media (max-width: 768px) {
  .projects {
    flex-direction: column; /* Stack projects vertically */
    overflow-x: hidden;
  }

  .project-container {
    grid-template-columns: 1fr; /* Stack details, desc, and image */
  }

  .desc {
    grid-column: 1 / 2;
  }
}

</style>


