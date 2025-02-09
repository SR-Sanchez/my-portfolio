<script setup lang="ts">
import HeroSection from '@/components/HeroSection.vue';

</script>

<template>
  <main>
    <HeroSection />
    <section id="projects">
            <h2 class="section-title">Featured Projects</h2>
            <div class="projects-grid">
                <article class="project-card">
                    <div class="project-image"></div>
                    <div class="project-content">
                        <h3 class="project-title">Health Tracker Portal</h3>
                        <div class="project-tags">
                            <span class="tag">Vue.js</span>
                            <span class="tag">Pinia</span>
                            <span class="tag">TypeScript</span>
                        </div>
                        <p>A user-friendly web app designed for tracking health metrics, scheduling and managing medical appointments, and previewing and downloading lab results.</p>
                    </div>
                </article>

                <article class="project-card">
                    <div class="project-image"></div>
                    <div class="project-content">
                        <h3 class="project-title">Breast Cancer Risk Assessment</h3>
                        <div class="project-tags">
                            <span class="tag">Nuxt</span>
                            <span class="tag">TypeScript</span>
                            <span class="tag">MariaDB</span>
                            <span class="tag">Php</span>
                        </div>
                        <p>A form that calculates breast cancer risk, checks for accurate responses, and determines eligibility for mammography, providing a test order in PDF and sending an automatic email with further details.</p>
                    </div>
                </article>

                <article class="project-card">
                    <div class="project-image"></div>
                    <div class="project-content">
                        <h3 class="project-title">Well-being App (personal project)</h3>
                        <div class="project-tags">
                            <span class="tag">React</span>
                            <span class="tag">Node.js</span>
                            <span class="tag">Gemini API</span>
                        </div>
                        <p>An AI-powered web platform offering evidence-based tools like thought records, sleep strategies and acceptance exercises in development, for independent or professional use.</p>
                    </div>
                </article>
            </div>
        </section>

        <section id="contact">
            <h2 class="section-title">Get in Touch</h2>
            <p>I'm always open to new opportunities and collaborations.</p>
            <div class="social-links">
                <a href="https://github.com/SR-Sanchez/" class="social-link"><i class="fab fa-github"></i></a>
                <a href="https://www.linkedin.com/in/sergio-ruiz-s%C3%A1nchez-5b3563150/" class="social-link"><i class="fab fa-linkedin"></i></a>
                <a href="https://wa.me/573015178499" class="social-link"><i class="fab fa-whatsapp"></i></a>
                <a href="mailto:sergioruizsanchezz@gmail.com" class="social-link"><i class="fas fa-envelope"></i></a>
            </div>
        </section>
  </main>
</template>
