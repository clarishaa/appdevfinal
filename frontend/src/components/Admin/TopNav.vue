<template>
    <!-- Navbar Start -->
    <nav class="navbar navbar-expand-lg bg-light navbar-light fixed-top p-0">
      <router-link to="/admin" class="navbar-brand d-flex align-items-center px-4 px-lg-5">
        <h1 class="m-0">La MinSU</h1>
      </router-link>
      <button type="button" class="navbar-toggler me-4" data-bs-toggle="collapse" data-bs-target="#navbarCollapse">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarCollapse">
        <div class="navbar-nav ms-auto p-4 p-lg-0">
          <router-link to="/" class="nav-item nav-link active fs-6">Dashboard</router-link>
          <div class="nav-item dropdown">
            <router-link to="#" class="nav-link dropdown-toggle fs-6" data-bs-toggle="dropdown">User Management</router-link>
            <div class="dropdown-menu bg-light m-0">
              <router-link to="/admin/staff" class="dropdown-item">Staff Management</router-link>
              <router-link to="/admin/customer" class="dropdown-item">Customer Management</router-link>
            </div>
          </div>
          <router-link to="/admin/inventory" class="nav-item nav-link fs-6">Inventory</router-link>
          <div class="nav-item dropdown">
            <router-link to="#" class="nav-link dropdown-toggle fs-6" data-bs-toggle="dropdown">Reservations</router-link>
            <div class="dropdown-menu bg-light m-0">
              <router-link to="/admin/pending-reservations" class="dropdown-item">Pending Reservations</router-link>
              <router-link to="/admin/cancelled-reservations" class="dropdown-item">Cancelled Reservations</router-link>
              <router-link to="/admin/confirmed-reservations" class="dropdown-item">Confirmed Reservations</router-link>
              <router-link to="/admin/payed-reservations" class="dropdown-item">Payed Reservations</router-link>
            </div>
          </div>
  
          <div class="nav-item dropdown">
            <router-link to="#" class="nav-link dropdown-toggle fs-6" data-bs-toggle="dropdown">
              <i class="fas fa-user fa-fw" style="color: forestgreen;"></i>
            </router-link>
            <div class="dropdown-menu bg-light m-0">
              <router-link to="/logout" class="dropdown-item">Logout</router-link>
            </div>
          </div>
        </div>
      </div>
  
      <form class="d-none d-md-inline-block form-inline ms-auto me-0 me-md-3 my-2 my-md-0">
        <div class="input-group mt-1">
          <input class="form-control" type="text" placeholder="Search for..." aria-label="Search for..."
            aria-describedby="btnNavbarSearch" />
          <button class="btn btn-primary" id="btnNavbarSearch" type="button"><i class="fas fa-search"></i></button>
        </div>
      </form>
    </nav>
    <!-- Navbar End -->
  </template>
  