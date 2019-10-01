<template>
  <div>
    <b-navbar toggleable="lg" type="dark" class="navbar-main">
      <b-container fluid>
        <b-navbar-brand href="#">
          <i class="fas fa-user-edit"></i>NavBar
        </b-navbar-brand>

        <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

        <b-collapse id="nav-collapse" is-nav>
          <b-navbar-nav class="ml-auto">
            <b-nav-item href="#">Link</b-nav-item>
            <b-nav-item href="#">Link</b-nav-item>
          </b-navbar-nav>
        </b-collapse>
      </b-container>
    </b-navbar>
  </div>
</template>
<script>
export default {
  name: "Navbar"
};
</script>
<style scoped lang="scss">
.navbar-main {
  background: #243e5e;
}
.fas {
  padding-right: 0.75rem;
}
.nav-item {
  padding: 0 1rem;
  font-size: 1.2rem;
}
</style>