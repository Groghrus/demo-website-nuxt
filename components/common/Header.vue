<template>
    <div class="header">
      <div class="container flex">
        <h1 class="logo md">Cloud Hosting</h1>
        <nav>
          <ul>
            <li>
              <nuxt-link to="/">Home</nuxt-link>
            </li>
            <li>
              <nuxt-link to="/features">Features</nuxt-link>
            </li>
            <li>
              <nuxt-link to="/docs">Documents</nuxt-link>
            </li>
          </ul>
        </nav>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Header',
  props: {},
  data() {
    return {};
  },
  computed: {}
};
</script>

<style lang="scss">
@import "../../assets/scss/main.scss";

.header {
  background: $primary-color;
  color: #fff;
  height: 70px;

  @include media-breakpoint-down(sm) {
    height: 120px;
  }

  ul {
    display: flex;

    @include media-breakpoint-down(sm) {
      padding: 10px;

    }
  }

  a {
    color: #fff;
    padding: 10px;
    margin: 0 5px;
    &:hover {
      border-bottom: 2px #fff solid;
    }
  }

  .flex {
    justify-content: space-between;

    @include media-breakpoint-down(sm) {
      flex-direction: column;
    }
  }
}

.logo {
  font-weight: 800;
}

</style>
