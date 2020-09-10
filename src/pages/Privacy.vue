<template>
  <Layout>
    <div class="container">
      <div class="contact-header">
        <h1 class="contact-title">Privacy Policy</h1>
        <p>Our apps in the Apple App Store do not collect or store any form of private data from the user.  Apple might collect data while using our Apps.  Please refer to Apple's Privacy Policies for more details.</p>
        <p><a href="https://www.apple.com/legal/privacy/">Apple Privacy Policy</a></p>
      </div>
    </div>
  </Layout>
</template>

<script>
export default {}
</script>

<style scoped>
.contact-header {
  padding: 5rem 0 4rem 0;
}
.contact-title {
  font-size: 4rem;
  margin: 0 0 4rem 0;
  padding: 0;
}
.button {
  color: var(--color-base);
  background: var(--color-contrast);
  outline: none;
  border: 0;
  font-size: 0.8rem;
  padding: 0.8rem 1.6rem;
  border-radius: 0.3rem;
  margin-top: 2rem;
  cursor: pointer;
  transition: opacity 0.25s ease;
  font-size: 500;
  letter-spacing: 0.035em;
}
.button:hover {
  opacity: 0.6;
}
.button:focus {
  border: 1px solid var(--color-base-1);
}
</style>
