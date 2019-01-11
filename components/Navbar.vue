<template>
  <div class="navbar">
    <div class="navbar__button">
      <div class="navbar__button--text">menu</div>
      <div class="navbar__button--icon">
        <div class="navbar__button--icon-line"></div>
        <div class="navbar__button--icon-line"></div>
        <div class="navbar__button--icon-line"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.navbar__button {
  position: fixed;
  right: 0;
  z-index: 10;
  display: flex;
  padding: 1rem;
  border: 1px solid var(--gray);
  align-items: baseline;
  cursor: pointer;
}

.navbar__button--text {
  text-transform: uppercase;
  font-weight: 600;
  font-size: 1.1rem;
}

.navbar__button--icon-line {
  width: 1rem;
  height: 3px;
  background-color: white;
  margin-top: 2px;
  margin-left: 0.5rem;
}
</style>
