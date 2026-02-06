<template>
  <div class="profile-page">
    <section class="container py-5">
      <div class="d-flex justify-content-end mb-4">
        <button @click="toggleTheme" class="btn btn-outline-secondary btn-sm">
          {{ isDarkMode ? '☀️ Light Mode' : '🌙 Dark Mode' }}
        </button>
      </div>

      <div class="row align-items-center">
        <div class="col-md-7">
          <small class="text-muted">2025</small>
          <h1 class="display-4 fw-bold">PORTFOLIO</h1>
          <p class="text-secondary fs-5">Computer Science Student</p>

          <p class="intro">
            Hi, I’m <strong>Terrence Josh Corpuz</strong>, a second-year Computer Science student Specializing in Cybersecurity and Forensics at
            <strong>Asia Pacific College</strong>. I’m passionate about web development, design,
            and building clean, functional digital experiences. I like playing Volleyball and any physical activities.
          </p>

          <div class="socials mt-3">
            <a href="https://github.com/tj082523" target="_blank"><i class="fab fa-github"></i></a>
            <a href="#" target="_blank"><i class="fab fa-linkedin"></i></a>
            <a href="https://www.facebook.com/terrence.josh.corpuz.2024/" target="_blank"><i class="fab fa-facebook"></i></a>
            <a href="mailto:tjcorpuz@student.apc.edu.ph"><i class="fas fa-envelope"></i></a>
          </div>
        </div>

        <div class="col-md-5 text-center mt-4 mt-md-0">
          <img src="/josh1x1.jpg" class="profile-img" alt="Profile" width="250" height="270">
        </div>
      </div>
    </section>

    <section class="container pb-5">
      <div class="row g-4">
        <div class="col-md-4">
          <div class="info-card">
            <h5>Education</h5>
            <p class="fw-semibold mb-1">BS Computer Science</p>
            <p class="text-muted mb-0">Asia Pacific College</p>
            <small class="text-muted">2024 – Present</small>
          </div>
        </div>

        <div class="col-md-4">
          <div class="info-card">
            <h5>Skills</h5>
            <ul>
              <li>HTML / CSS</li>
              <li>Python</li>
              <li>Basic SQL</li>
              <li>XAMPP</li>
            </ul>
          </div>
        </div>

        <div class="col-md-4">
          <div class="info-card">
            <h5>Interests</h5>
            <ul>
              <li>Web Development</li>
              <li>Minimal Design</li>
              <li>Technology</li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <section class="container pb-5">
      <h5 class="mb-4"><i class="far fa-images me-2"></i>Gallery</h5>
      <div class="gallery-scroll">
        <img src="public/images/josh.jpg" alt="Coding" width="250" height="270">
        <img src="public/images/apcmvt.JPG" alt="Design" width="250" height="270">
        <img src="public/images/hehe.jpg" alt="Technology" width="250" height="270">
        <img src="public/images/bebe.jpg" alt="Volleyball" width="250" height="270">
        <img src="public/images/roxxy.jpg" alt="Coffee" width="250" height="270">
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "PersonalProfile",
  data() {
    return {
      isDarkMode: false
    };
  },
  mounted() {
    // Check local storage when the component loads
    if (localStorage.getItem("theme") === "dark") {
      this.isDarkMode = true;
      document.body.classList.add("dark-mode");
    }
  },
  methods: {
    toggleTheme() {
      this.isDarkMode = !this.isDarkMode;
      
      if (this.isDarkMode) {
        document.body.classList.add("dark-mode");
        localStorage.setItem("theme", "dark");
      } else {
        document.body.classList.remove("dark-mode");
        localStorage.setItem("theme", "light");
      }
    }
  }
}
</script>

<style src="./css/personalprofile.css"></style>