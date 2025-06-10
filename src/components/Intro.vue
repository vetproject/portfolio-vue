<template>
  <div class="intro">
    <h1>YOUERN RIN</h1>
    <h2>FRONT END SOFTWARE ENGINEER</h2>
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
  margin: 0; /* Remove margin */
}
ថ
.intro h1 {
  font-size: 4rem;
  font-weight: bold;
  margin-bottom: 0; /* Remove margin */
  font-family: 'Georgia', serif;
  margin: 0; /* Remove all margin */
}

.intro h2 {
  font-size: 1.3rem;
  font-weight: bold;
  margin-bottom: 0; /* Remove margin */
  letter-spacing: 1px;
  margin: 0; /* Remove all margin */
}
</style>