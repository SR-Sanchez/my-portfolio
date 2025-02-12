<template>
  <section id="hero">
    <div class="hero-content">
      <h1>Hi, I'm <span class="highlight">Sergio Ruiz</span></h1>
      <div class="subtitle-container">
        <p class="subtitle">Jr. Full Stack Developer specializing in front-end development, with a strong background in
          psychology and neuropsychology.
        </p>
        <p class="subtitle">
          Passionate about creating digital solutions that promote mental health, well-being, and personal growth.
        </p>
      </div>
      <a href="#contact" class="cta-button">Get in touch</a>
    </div>
    <div class="hero-image">
      <img src="@/assets/images/profile_01.png" alt="Your profile picture">
    </div>
  </section>
</template>

<style lang="css" scoped>
.cta-button {
  margin-top: 20px;
}

.subtitle-container {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.subtitle {
  margin-bottom: 0px;
}
</style>
