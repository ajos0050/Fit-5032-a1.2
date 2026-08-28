<script setup></script>

<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-success">
      <div class="container">
        <a class="navbar-brand fw-bold" href="#">Patch Melbourne</a>

        <!-- Mobile hamburger button -->
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#patchNavbar"
          aria-controls="patchNavbar"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <!-- Navigation links -->
        <div class="collapse navbar-collapse" id="patchNavbar">
          <div class="navbar-nav ms-auto">
            <a class="nav-link active" href="#home">Home</a>
            <a class="nav-link" href="#find-plants">Find Plants</a>
            <a class="nav-link" href="#my-patch">My Green Patch</a>
            <a class="nav-link" href="#get-involved">Get Involved</a>
            <a class="nav-link" href="#learn">Learn</a>
            <a class="nav-link" href="#about">About</a>
          </div>
        </div>
      </div>
    </nav>

    <main id="home">
      <section class="hero-section">
        <div class="container text-center">
          <h1 class="display-4 fw-bold">
            Grow biodiversity where you live
          </h1>

          <p class="lead hero-description">
            Turn your balcony, courtyard or garden into a green patch
            that supports Melbourne's native biodiversity.
          </p>

          <a href="#find-plants" class="btn btn-success btn-lg">
            Find Native Plants
          </a>
        </div>
      </section>

      <section id="find-plants" class="py-5 bg-light">
        <div class="container text-center">
          <h2 class="fw-bold">Find Plants</h2>
          <p class="text-muted">
            Find native plants suited to your space and growing conditions.
          </p>
        </div>
      </section>
    </main>
  </div>
</template>

<style scoped>
.hero-section {
  min-height: 65vh;
  display: flex;
  align-items: center;
  padding: 4rem 1rem;
}

.hero-description {
  max-width: 650px;
  margin: 1.5rem auto;
}

/* Small phones */
@media (max-width: 576px) {
  .hero-section {
    min-height: 55vh;
    padding: 3rem 1rem;
  }

  .hero-section h1 {
    font-size: 2.2rem;
  }
}
</style>
