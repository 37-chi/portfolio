<template>
  <div>
    <b-navbar type="dark" class="navba"  fixed="top">>
      <b-navbar-nav  >
        <b-nav-item href="#">Home</b-nav-item>
        <!-- Navbar dropdowns -->
        <b-nav-item-dropdown text="Lang" right>
          <b-dropdown-item href="#">EN</b-dropdown-item>
        </b-nav-item-dropdown>
        <b-nav-item-dropdown text="User" right>
          <b-dropdown-item href="#">Account</b-dropdown-item>
        </b-nav-item-dropdown>
      </b-navbar-nav>
    </b-navbar>
  </div>
</template>


<style scoped>
.navba {
  color: rgb(0, 0, 0);
  background-color: transparent;
  border-color: transparent;
}
.navbar li { color: rgb(126, 68, 68);
  background-color: transparent;
  border-color: transparent; } 
  .wrapper {
  position: sticky;
  top: 0;
}
</style>
