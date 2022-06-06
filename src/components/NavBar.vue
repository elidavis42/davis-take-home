<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand">Random Facts</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav me-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link" href="https://uselessfacts.jsph.pl/">
            About</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href=""
          data-bs-toggle="modal" data-bs-target="#exampleModal">Contact Us</a>
        </li>
      </ul>
      <div class="d-flex">
        <input class="form-control me-2" input type="email" placeholder="Email" aria-label="email">
        <input class="form-control me-2" input type="password" placeholder="Password" aria-label="password">
        <button class="btn btn-outline-success me-2"
         data-bs-toggle="modal" data-bs-target="#exampleModal">
          Login</button>
        <button class="btn btn-outline-info"
         data-bs-toggle="modal" data-bs-target="#exampleModal">Signup</button>
      </div>
    </div>
  </div>
</nav>
<SorryModal/>
</template>

<script>

import SorryModal from './SorryModal.vue'

export default {
  name: 'NavBar',
  components: {
    SorryModal,
  },
}
</script>

