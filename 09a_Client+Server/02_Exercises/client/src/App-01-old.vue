<template>
  <div id="app">
    <div id="nav">
      <router-link to="/home">Home</router-link> |
      <router-link to="/message">Message</router-link> |
      <!-- Decoupling Params with Props -->
      <router-link to="/messages">Message Feed</router-link> |
      <!-- Passing Route Parameters -->
      <router-link :to="{ name: 'about', params: { user: 'of Hans Muster'}}">About</router-link>
    </div>
    <router-view/>
    <MyNavigation />
  </div>



</template>
<script>
import SimpleNav from "./components/SimpleNav";

export default {
  name: 'app',
  components: {
    MyNavigation: SimpleNav,
  }
}
</script>


