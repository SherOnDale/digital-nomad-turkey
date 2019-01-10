<template>
  <div class="home">
    <div class="home__hero--container">
      <div class="home__hero">
        <div class="home__hero--logo">
          <img src="/images/logo.png" alt="Digital Nomad Turkey Logo">
        </div>
        <div class="home__hero--title">
          <h1>digital nomad turkey</h1>
        </div>
        <div class="home__hero--subtitle">
          <p>nullam ultrices. neque et faucibus viverba</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.home__hero--container {
  height: 100vh;
  width: 100vw;
  background: url(/images/banner-desktop.jpg) center no-repeat;
  background-size: cover;
  clip-path: polygon(0 0, 100% 0, 100% 90%, 10% 100%, 0% 100%);
}

.home__hero--container:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  width: 100vw;
  height: 100vh;
  background: var(--primary-trans);
  clip-path: polygon(0 0, 100% 0, 100% 90%, 10% 100%, 0% 100%);
}

.home__hero {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  height: 23vh;
  width: 60vw;
  z-index: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.home__hero--logo img {
  height: 4rem;
}

.home__hero--title {
  border-bottom: 1px solid var(--gray);
  padding-bottom: 1.5rem;
}

.home__hero--title h1 {
  text-transform: uppercase;
  font-weight: 700;
  letter-spacing: 0.3rem;
}

.home__hero--subtitle p {
  text-transform: uppercase;
  color: var(--gray);
  letter-spacing: 0.1rem;
}
</style>
