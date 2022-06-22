<template>
  <div id="app">

      <b-navbar toggleable="lg" type="dark" variant="info">
        <b-navbar-brand href="#"><router-link to="/home">Home</router-link></b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav>
            <b-nav-item><router-link :to="{ name: 'about', params: { user: 'of Hans Muster'}}">About us</router-link></b-nav-item>
            <b-nav-item><router-link to="/messages">Shoppinglist</router-link></b-nav-item>
            <!-- Passing Route Parameters -->
            <b-nav-item><router-link to="/message">Warenkorb</router-link></b-nav-item>
            <!-- Decoupling Params with Props -->
          </b-navbar-nav>
        </b-collapse>
      </b-navbar>
    <router-view/>
    <MyNavigation />
  </div>


</template>


