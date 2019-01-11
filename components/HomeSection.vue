<template>
  <div
    class="home__section"
    :style="{zIndex: index, top: top, transform: `skew(0deg, ${skew}`}"
    :class="{'home__section--bg': !gradient, 'home__section--gradient': gradient}"
  >
    <div
      class="home__section--container"
      :style="{transform: `translate(-50%, -50%) skew(0deg, ${skewOpp}`}"
    >
      <div class="home__section--avatar" :style="{order: order}">
        <img :src="content.imageUrl" alt="image">
      </div>
      <div class="home__section--body" :style="{textAlign: textAlignment}">
        <div class="home__section--title">
          <h2>{{content.title}}</h2>
        </div>
        <div class="home__section--subtitle">{{content.subtitle}}</div>
        <div class="home__section--action">learn more</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    index: Number,
    top: String,
    content: Object,
    gradient: {
      type: Boolean,
      default: true
    },
    skew: {
      type: String,
      default: "0deg"
    },
    skewOpp: {
      type: String,
      default: "0deg"
    },
    order: {
      type: Number,
      default: 1
    },
    textAlignment: {
      type: String,
      default: "left"
    }
  }
};
</script>

<style>
.home__section {
  position: absolute;
  width: 100%;
  height: 70vh;
  background-color: red;
}

.home__section--bg {
  background-color: var(--accent-one);
}

.home__section--gradient {
  background: linear-gradient(
    to bottom,
    var(--accent-two) 0%,
    var(--accent-two) 10%,
    var(--accent-one) 40%
  );
}

.home__section--container {
  position: absolute;
  top: 50%;
  left: 50%;
  width: 70vw;
  display: flex;
  justify-content: space-between;
}

.home__section--avatar img {
  border-radius: 50%;
}

.home__section--body {
  width: 50vw;
}

.home__section--title,
.home__section--action {
  text-transform: uppercase;
}

.home__section--title {
  border-bottom: 1px solid var(--gray);
}

.home__section--title h2 {
  letter-spacing: 0.2rem;
  padding-bottom: 1.2rem;
}
</style>
