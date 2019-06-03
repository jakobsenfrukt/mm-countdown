<template>
  <div>
    <Gradient />
    <nuxt />
    <footer class="site-footer">
      <Newsletter heading="Be the first to know" />
      <nav class="footer-nav">
        <a href="https://www.mmstore.com/pages/privacy-policy">Cookies</a>
        <nuxt-link to="/contact">Contact our team</nuxt-link>
        <a href="https://jakobsenfrukt.no" class="credit">Website by JF&amp;G 🍌</a>
      </nav>
    </footer>
  </div>
</template>

<script>
import Gradient from '~/components/Gradient.vue'
import Newsletter from '~/components/Newsletter.vue'

export default {
  layout: 'countdown',
  components: {
    Gradient,
    Newsletter
  }
}
</script>

<style lang="scss" scoped>
@import '@/assets/css/variables.scss';
a.index {
  display: block;
  text-align: left;
  opacity: 0.5;
  text-decoration: none;
  padding: 0.5rem 1rem;
  font-style: italic;
  text-transform: uppercase;

  &:hover {
    opacity: 1;
  }
}
.site-footer {
  width: 100%;
  padding: 8rem 1rem 1rem;
  position: relative;
  font-size: $font-s;
  background: black;
}
.to-top {
  display: block;
  text-decoration: none;
  text-transform: uppercase;
  font-weight: 700;
  letter-spacing: 0.05em;
  margin-bottom: 3rem;

  .icon {
    font-size: 3rem;
    width: 3rem;
    margin: 0 auto;
    transform: rotate(-43deg);
  }
}
.footer-nav {
  display: flex;

  a {
    display: inline-block;
    margin: 0 1rem;
    text-decoration: none;
    text-transform: uppercase;
    font-weight: 700;
    font-size: 12px;
    line-height: 1;
    font-style: italic;
    letter-spacing: 0.05em;
    opacity: 0.5;

    &:hover {
      color: $color-theme-light;
    }

    &.credit {
      margin-left: auto;
    }
  }
}

@media (max-width: $media-s) {
  .footer-nav a {
    margin: 0 0.5rem;
    font-size: 10px;
  }
}
</style>
