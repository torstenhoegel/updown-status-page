<template>
  <div
    id="app"
    class="container"
  >
    <!-- header-->
    <div class="row align-items-center">
      <div class="col-md-12 text-center">
        <div class="top">
          <a :href="$config.website_url"><img
            v-if="typeof $config.logo_url !== 'undefined'"
            :src="$config.logo_url"
            :alt="$config.website_name"
            class="logotop"
          ></a>
          <h3>{{ $config.website_name }} Status Page</h3>
        </div>
      </div>
    </div>
    <!-- content -->
    <StatusPage />
    <!-- footer -->
    <div class="row text-center footer">
      <div
        v-if="typeof $config.website_url === 'string'"
        class="col"
      >
        <a :href="$config.website_url">&#8249; Home</a>
      </div>
      <div class="col">
        <a href="https://help.go-on.io" target="_blank">Help</a>
      </div>
    </div>
  </div>
</template>

<script>
import StatusPage from './components/StatusPage'

export default {
  name: 'App',
  components: {
    StatusPage
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.logotop {
  max-height: 80px;
  margin-bottom: 20px;
}
.top {
  padding: 20px 0;
  padding-top: 0px;
}
.footer {
  padding: 35px 0 20px 0;
}
</style>
