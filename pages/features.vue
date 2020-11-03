<template>
  <main>
    <section class="features-head bg-primary py-3">
      <div class="container grid">
        <div>
          <h1 class="xl">Features</h1>
          <p class="lead">Check out the features of Cloud Hosting that separate us from the
            competition
          </p>
        </div>
        <img src="~/assets/images/server.png" alt="pic">
      </div>
    </section>
    <section class="features-sub-head bg-light py-3">
      <div class="container grid">
        <div>
          <h1 class="md">The Cloud Hosting Platform</h1>
          <p class="lead">Check out the features of Cloud Hosting that separate us from the
            competition
          </p>
        </div>
        <img src="~/assets/images/server2.png" alt="pic">
      </div>
    </section>
    <section class="features-main my-2">
      <div class="container grid grid-3">
        <div class="card flex">
          <font-awesome-icon :icon="['fas', 'server']" size="3x"/>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing.</p>
        </div>
        <div class="card flex">
          <font-awesome-icon :icon="['fas', 'network-wired']" size="3x"/>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga minima nesciunt porro quidem, recusandae temporibus.</p>
        </div>
        <div class="card flex">
          <font-awesome-icon :icon="['fas', 'laptop-code']" size="3x"/>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Laboriosam, quaerat.</p>
        </div>
        <div class="card flex">
          <font-awesome-icon :icon="['fas', 'database']" size="3x"/>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam, similique.</p>
        </div>
        <div class="card flex">
          <font-awesome-icon :icon="['fas', 'power-off']" size="3x"/>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam asperiores consequuntur, dolor ipsam placeat quae saepe similique sint tempore totam?</p>
        </div>
        <div class="card flex">
          <font-awesome-icon :icon="['fas', 'upload']" size="3x"/>
          <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Atque error fuga laboriosam laudantium odio placeat sint voluptate. Commodi distinctio, dolore eum ipsam nostrum optio porro.</p>
        </div>
      </div>
    </section>
  </main>
</template>

<script>
export default {
  name: 'features',
  props: {},
  data() {
    return {};
  },
  computed: {}
};
</script>

<style lang="scss">
.features-head {
  img {
    width: 200px;
    justify-self: flex-end;
  }
}

.features-sub-head {
  img {
    width: 300px;
    justify-self: flex-end;
  }
}

.features-main {
  .card > svg {
    margin-right: 20px;
  }

  .grid {
    padding: 30px;

    & > *:first-child {
      grid-column: 1 / span 3;
    }

    & > *:nth-child(2) {
      grid-column: 1 / span 2;
    }

  }
}
</style>
