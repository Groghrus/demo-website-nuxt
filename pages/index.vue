<template>
  <main>
    <section class="showcase">
      <div class="container grid">
        <div class="showcase-text">
          <h1>Easier Deployment</h1>
          <p>Deploy web apps of all kinds, from large scale enterprise APIs to static websites for individuals. Fill out
            the form to try a demo of our platform</p>
          <nuxt-link to="/features" class="btn btn-outline">Read More</nuxt-link>
        </div>
        <div class="showcase-form card">
          <h2>Request a Demo</h2>
          <form name="contact">
            <div class="form-control">
              <input type="text" name="name" placeholder="Name" class="inpt-field" required>
            </div>
            <div class="form-control">
              <input type="text" name="company" placeholder="Company Name" class="inpt-field" required>
            </div>
            <div class="form-control">
              <input type="email" name="email" placeholder="Email" class="inpt-field" required>
            </div>
            <input type="submit" value="Send" class="btn btn-primary">
          </form>
        </div>
      </div>
    </section>
    <section class="stats">
      <div class="container">
        <h3 class="stats-heading text-center my-1">
          Welcome to the best platform for building applications of all types with modern architecture and scaling
        </h3>
        <div class="grid grid-3 text-center my-4">
          <div>
            <font-awesome-icon :icon="['fas', 'server']" size="3x"/>
            <h3>10,349,405</h3>
            <p class="text-secondary">Deployments</p>
          </div>
          <div>
            <font-awesome-icon :icon="['fas', 'upload']" size="3x"/>
            <h3>987 TB</h3>
            <p class="text-secondary">Published</p>
          </div>
          <div>
            <font-awesome-icon :icon="['fas', 'project-diagram']" size="3x"/>
            <h3>2,343,265</h3>
            <p class="text-secondary">Projects</p>
          </div>
        </div>
      </div>
    </section>
    <section class="cli">
      <div class="container grid">
        <img src="~/assets/images/cli.png" alt="pic">
        <div class="card">
          <h3>Easy to use, cross platform CLI</h3>
        </div>
        <div class="card">
          <h3>Deploy in seconds</h3>
        </div>
      </div>
    </section>
    <section class="cloud bg-primary my-2 py-2">
      <div class="container grid">
        <div class="text-center">
          <h2 class="lg">Extreme Cloud Hosting</h2>
          <p class="lead my-1">Cloud hosting like you've never seen. Fast, efficient and scalable</p>
          <nuxt-link to="/features" class="btn btn-dark">Read More</nuxt-link>
        </div>
        <img src="~/assets/images/cloud.png" alt="cloud">
      </div>
    </section>
    <section class="languages">
      <h2 class="md text-center my-2">
        Supported Languages
      </h2>
      <div class="container flex">
        <div class="card" v-for="card in cards">
          <h4>{{card.title}}</h4>
          <img :src="card.src" alt="pic">
        </div>
      </div>
    </section>
  </main>
</template>

<script>


export default {
  name: 'Home',
  components: {},
  props: {},
  data() {
    return {
      cards: [
        {title: 'Node.js', src: require('../assets/images/logos/node.png')},
        {title: 'Python', src: require('../assets/images/logos/python.png')},
        {title: 'C#', src: require('../assets/images/logos/csharp.png')},
        {title: 'Ruby', src: require('../assets/images/logos/ruby.png')},
        {title: 'PHP', src: require('../assets/images/logos/php.png')},
        {title: 'Scala', src: require('../assets/images/logos/scala.png')},
        {title: 'Clojure', src: require('../assets/images/logos/clojure.png')},
      ]
    };
  },
  computed: {}
};
</script>

<style lang="scss">

.showcase {
  height: 400px;
  background-color: $primary-color;
  color: #fff;
  position: relative;

  @include media-breakpoint-down(md) {
    height: auto;
  }

  &::before, &::after {
    content: '';
    position: absolute;
    height: 100px;
    bottom: -70px;
    right: 0;
    left: 0;
    background: #fff;
    transform: skewY(-3deg);
  }

  h1 {
    font-size: 40px;
  }

  p {
    margin: 20px 0;
  }

  .grid {
    overflow: visible;
    grid-template-columns: 55% auto;
    gap: 30px;
  }

  &-text {
    @include media-breakpoint-down(md) {
      margin-top: 40px;
    }
  }

  &-form {
    position: relative;
    top: 60px;
    height: 350px;
    width: 400px;
    padding: 40px;
    z-index: 100;
    justify-self: flex-end;

    @include media-breakpoint-down(md) {
      justify-self: center;
      margin: auto;
    }

    @include media-breakpoint-down(sm) {
      width: 300px;
    }

    .form-control {
      margin: 30px 0;
    }

    input[type='text'], input[type='email'], .inpt-field {
      border: 0;
      border-bottom: 1px solid #b4becb;
      width: 100%;
      padding: 3px;
      font-size: 16px;
    }

    input:focus {
      outline: none;
    }

    h2 {
      font-size: 24px;
    }
  }
}

.stats {
  padding-top: 100px;

  &-heading {
    max-width: 500px;
    margin: auto;
  }

  .grid {

    h3 {
      font-size: 35px;
    }

    p {
      font-size: 20px;
      font-weight: 900;
    }
  }
}

.cli {
  .grid {
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);

    & > *:first-child {
      grid-column: 1 / span 2;
      grid-row: 1 / span 2;
    }


  }
}

.cloud {
  .grid {
    grid-template-columns: 4fr 3fr;
  }
}

.languages {
  .flex {
    flex-wrap: wrap;
  }

  .card {
    text-align: center;
    margin: 18px 10px 40px;
    transition: transform 0.2s ease-in;

    &:hover {
      transform: translateY(-15px);
    }

    h4 {
      font-size: 20px;
      margin-bottom: 10px;
    }
  }
}

</style>
