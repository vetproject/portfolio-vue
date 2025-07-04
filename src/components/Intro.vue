<template>
  <div class="intro">
    <h1>YOUERN RIN</h1>
    <h2>WEB DEVELOPER</h2>
    <p class="intro-desc">
      Passionate about building modern, responsive web applications using Vue.js and other cutting-edge technologies.<br>
      Experienced in frontend and backend development, UI/UX design, and agile workflows.<br>
      Let's work together to create something amazing!
    </p>
    <ul class="intro-skills">
      <li>Vue.js</li>
      <li>JavaScript (ES6+)</li>
      <li>HTML5 &amp; CSS3</li>
      <li>Node.js</li>
      <li>REST APIs</li>
      <li>Git &amp; GitHub</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'IntroPort'
}
</script>

<style scoped>
.intro {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: linear-gradient(135deg, #1e90ff 0%, #6a11cb 100%);
  color: #fff;
  text-align: center;
  position: relative;
  margin: 0;
}

.intro h1 {
  font-size: 4rem;
  font-weight: bold;
  margin: 0;
  font-family: 'Georgia', serif;
}

.intro h2 {
  font-size: 1.3rem;
  font-weight: bold;
  margin: 0;
  letter-spacing: 1px;
}

.intro-desc {
  margin: 1.5rem 0 1rem 0;
  font-size: 1.1rem;
  max-width: 500px;
  line-height: 1.6;
}

.intro-skills {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  justify-content: center;
}

.intro-skills li {
  background: rgba(255,255,255,0.15);
  border-radius: 20px;
  padding: 0.5rem 1.2rem;
  font-size: 1rem;
  font-weight: 500;
}
</style>