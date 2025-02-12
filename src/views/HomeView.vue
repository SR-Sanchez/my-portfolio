<script setup lang="ts">
import { ref } from 'vue';
import HeroSection from '@/components/HeroSection.vue';
const showVideo1 = ref(false);
const showVideo2 = ref(false);
const show1of2 = ref(true);
const openLink = () => {
  window.open('https://mindguide.netlify.app/', '_blank')
}
</script>

<template>
  <main>
    <HeroSection />
    <section id="projects">
      <h2 class="section-title">Featured Projects</h2>
      <div class="projects-grid">
        <article class="project-card">
          <div class="project-image">
            <img src="@/assets/images/Vector.png" class="image" alt="project image" @click="showVideo1 = true" />
          </div>
          <div class="project-content">
            <h3 class="project-title">Health Tracker Portal</h3>
            <div class="project-tags">
              <span class="tag">Vue.js</span>
              <span class="tag">Pinia</span>
              <span class="tag">TypeScript</span>
            </div>
            <p>A user-friendly web app designed for tracking health metrics, scheduling and managing medical
              appointments, and previewing and downloading lab results.</p>
          </div>
        </article>

        <article class="project-card">
          <div class="project-image">
            <img src="@/assets/images/Vector2.png" class="image" alt="project image" @click="showVideo2 = true" />
          </div>
          <div class="project-content">
            <h3 class="project-title">Breast Cancer Risk Assessment</h3>
            <div class="project-tags">
              <span class="tag">Nuxt</span>
              <span class="tag">TypeScript</span>
              <span class="tag">MariaDB</span>
              <span class="tag">Php</span>
            </div>
            <p>A form that calculates breast cancer risk, checks for accurate responses, and determines eligibility for
              mammography, providing a test order in PDF and sending an automatic email with further details.</p>
          </div>
        </article>

        <article class="project-card">
          <div class="project-image">
            <img src="@/assets/images/chat_bot.png" class="image" alt="project image" @click="openLink" />
          </div>
          <div class="project-content">
            <h3 class="project-title">Well-being App (personal project)</h3>
            <div class="project-tags">
              <span class="tag">React</span>
              <span class="tag">Node.js</span>
              <span class="tag">Gemini API</span>
            </div>
            <p>An AI-powered web platform offering evidence-based tools like thought records, sleep strategies and
              acceptance exercises in development, for independent or professional use.</p>
          </div>
        </article>
      </div>
    </section>

    <section id="contact">
      <h2 class="section-title">Get in Touch</h2>
      <p>I'm always open to new opportunities and collaborations.</p>
      <div class="social-links">
        <a href="https://github.com/SR-Sanchez/" class="social-link"><i class="fab fa-github"></i></a>
        <a href="https://www.linkedin.com/in/sergio-ruiz-s%C3%A1nchez-5b3563150/" class="social-link"><i
            class="fab fa-linkedin"></i></a>
        <a href="https://wa.me/573015178499" class="social-link"><i class="fab fa-whatsapp"></i></a>
        <a href="mailto:sergioruizsanchezz@gmail.com" class="social-link"><i class="fas fa-envelope"></i></a>
      </div>
    </section>
    <div class="drop-down" v-if="showVideo1">
      <p class="video-text">{{ show1of2 ? 'Video 1/2' : 'Video 2/2' }}</p>
      <div class="video-container">
        <img src="@/assets/icons/chevron-left.svg" @click="show1of2 = true">
        <iframe v-if="show1of2" width="560" height="315" src="https://www.youtube.com/embed/P2IcJXpubRE?vq=hd720"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
        <iframe v-else width="560" height="315" src="https://www.youtube.com/embed/7Ri7MISqHVI?vq=hd720" frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
        <img src="@/assets/icons/chevron-right.svg" @click="show1of2 = false">
      </div>
      <div class="nav-container">
         <img src="@/assets/icons/chevron-left.svg" @click="show1of2 = true">
         <button @click="showVideo1 = false, show1of2 = true" class="btn">Close</button>
         <img src="@/assets/icons/chevron-right.svg" @click="show1of2 = false">
      </div>

    </div>
    <div class="drop-down" v-if="showVideo2">
      <p class="video-text">{{ show1of2 ? 'Video 1/2' : 'Video 2/2' }}</p>
      <div class="video-container">
        <img src="@/assets/icons/chevron-left.svg" @click="show1of2 = true">
        <iframe v-if="show1of2" width="560" height="315" src="https://www.youtube.com/embed/0akavNTU0ec?vq=hd720"
          frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
        <iframe v-else width="560" height="315" src="https://www.youtube.com/embed/bwBDoXja6Tc?vq=hd720" frameborder="0"
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
          allowfullscreen>
        </iframe>
        <img src="@/assets/icons/chevron-right.svg" @click="show1of2 = false">
      </div>
      <div class="nav-container">
         <img src="@/assets/icons/chevron-left.svg" @click="show1of2 = true">
         <button @click="showVideo2 = false, show1of2 = true" class="btn">Close</button>
         <img src="@/assets/icons/chevron-right.svg" @click="show1of2 = false">
      </div>

    </div>
  </main>
</template>

<style lang="css" scoped>
#projects {
  position: relative;
}

.project-image {
  display: flex;
  justify-content: center;
  cursor: pointer;
}

img {
  height: 200px;
  border-radius: 16px 16px 0 0;
}

.video-container {
  display: flex;
  align-items: center;
  gap: 16px;

  img {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 60px;
    border-radius: 48px;
    background-color: white;
  }

  img:hover {
    cursor: pointer
  }
}

.video-text {
  color: #413D35;
  font-weight: 600;
  padding: 8px 16px;
  background-color: white;
  border-radius: 16px;
}

.btn {
  display: inline-block;
  padding: 0.75rem 1.5rem;
  background: var(--primary);
  color: white;
  text-decoration: none;
  border-radius: 0.5rem;
  font-weight: 500;
  transition: background 0.3s;
}

.btn:hover {
  background: #1d4ed8;
  cursor: pointer;
}

@media (min-width: 741px){
  .nav-container{
    img{
      display: none;
    }
  }
}

@media (max-width: 740px){
  .video-container{
    max-width: 80%;
    img{
      display: none;
    }
  }

  .nav-container{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    gap: 24px;
    img{
      height: 40px;
      border-radius: 48px;
      background-color: white;
      }
  }

}
</style>
