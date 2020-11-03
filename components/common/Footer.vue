<template>
  <div class="footer bg-dark py-5">
    <div class="container grid grid-3">
      <div>
        <h1 class="logo md">Cloud Hosting</h1>
        <p>Copyright &copy; 2020</p>
      </div>
      <nav>
        <ul>
          <li>
            <nuxt-link class="ihover" to="/">Home</nuxt-link>
          </li>
          <li>
            <nuxt-link class="ihover" to="/features">Features</nuxt-link>
          </li>
          <li>
            <nuxt-link class="ihover" to="/docs">Documents</nuxt-link>
          </li>
        </ul>
      </nav>
      <div class="social">
        <a href="#"><font-awesome-icon class="ihover" :icon="['fab', 'github']" size="2x"/></a>
        <a href="#"><font-awesome-icon class="ihover" :icon="['fab', 'facebook']" size="2x"/></a>
        <a href="#"><font-awesome-icon class="ihover" :icon="['fab', 'instagram']" size="2x"/></a>
        <a href="#"><font-awesome-icon class="ihover" :icon="['fab', 'twitter']" size="2x"/></a>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
  props: {},
  data() {
    return {};
  },
  computed: {}
};
</script>

<style lang="scss">

.footer {
  flex-shrink: 0;
  .social a {
    margin: 0 10px;
  }
}

</style>
