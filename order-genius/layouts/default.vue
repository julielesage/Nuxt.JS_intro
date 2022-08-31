<template>
  <div>
    <nav class="navbar navbar-dark bg-dark">
      <ul class="navbar-nav">
        <li class="nav-item active">
          <nuxt-link class="nav-link" to="/">Home</nuxt-link>
        </li>
        <li class="nav-item">
          <nuxt-link class="nav-link" to="/orders">Orders</nuxt-link>
        </li>
      </ul>
    </nav>

    <div class="container">
      <nuxt />
    </div>
  </div>
</template>
