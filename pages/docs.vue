<template>
  <main>
    <section class="docs-head bg-primary py-3">
      <div class="container grid">
        <div>
          <h1 class="xl">Docs</h1>
          <p class="lead">
            Learn how to work with the Cloud Hosting platform
          </p>
        </div>
        <img src="~/assets/images/docs.png" alt="doc">
      </div>
    </section>
    <section class="docs-main my-4">
      <div class="container grid">
        <div class="card bg-light p-3">
          <h3 class="my-2">Essentials</h3>
          <nav>
            <ul>
              <li>
                <nuxt-link class="ihover" to="/">Introduction</nuxt-link>
              </li>
              <li>
                <nuxt-link class="ihover" to="#">About Cloud Hosting</nuxt-link>
              </li>
              <li>
                <nuxt-link class="ihover" to="#">Installation</nuxt-link>
              </li>
            </ul>
          </nav>

          <h3 class="my-2">Deployment</h3>
          <nav>
            <ul>
              <li>
                <nuxt-link class="ihover" to="#">Setting up a container</nuxt-link>
              </li>
              <li>
                <nuxt-link class="ihover" to="#">Using the CLI</nuxt-link>
              </li>
              <li>
                <nuxt-link class="ihover" to="#">Managing resources</nuxt-link>
              </li>
              <li>
                <nuxt-link class="ihover" to="#">Upgrade & downgrade</nuxt-link>
              </li>
            </ul>
          </nav>
        </div>
        <div class="card">
          <h3>Introduction</h3>
          <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Distinctio illo facere perferendis laborum?
            Similique
            recusandae incidunt eos dolorum aliquam ipsam unde perspiciatis laudantium totam quam laborum velit, at
            maxime
            minus?</p>

          <div class="alert alert-success">
            <font-awesome-icon :icon="['fas', 'info']"/>
            Lorem ipsum dolor sit amet, consectetur.
          </div>
          <h3>Lorem, ipsum dolor.</h3>
          <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Minima totam magni eius vitae velit id, atque
            veritatis! At, vero porro.</p>
          <nuxt-link to="#" class="btn btn-primary">Install CLI</nuxt-link>

          <h3>Requirements</h3>
          <ul>
            <li>Windows 10, Mac OSX, Linux</li>
            <li>Node.js v12 or higher</li>
          </ul>

          <h3>Install</h3>
          <p>Mac (Homebrew)</p>
          <pre><code>$ brew install cloud-hosting-cli</code></pre>
          <p>NPM</p>
          <pre><code>$ npm install cloud-hosting-cli</code></pre>
          <p>Yarn</p>
          <pre><code>$ yarn install cloud-hosting-cli</code></pre>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'docs',
  props: {},
  data() {
    return {};
  },
  computed: {}
};
</script>

<style lang="scss">
.docs-head {
  img {
    width: 200px;
    justify-self: flex-end;
  }
}

.docs-main {
  h3 {
    margin: 20px 0;
    font-weight: 600;
    font-size: 22px;
  }

  .grid {
    grid-template-columns: 1fr 2fr;
    align-items: flex-start;

    nav li {
      font-size: 16px;
      padding-bottom: 5px;
      margin-bottom: 5px;
      border-bottom: 1px #ccc solid;
    }
  }

  .nuxt-link-exact-active {
    color: $dark-color;
  }

}
</style>
