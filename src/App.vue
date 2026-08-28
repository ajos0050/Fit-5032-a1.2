<script setup></script>

<template>
  <div>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg bg-success navbar-dark">
      <div class="container">
        <a class="navbar-brand fw-bold" href="#">Patch Melbourne</a>

        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#mainNavbar"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <div id="mainNavbar" class="collapse navbar-collapse">
          <div class="navbar-nav ms-auto">
            <a class="nav-link" href="#plant-finder">Plant Finder</a>
            <a class="nav-link" href="#my-patch">My Green Patch</a>
            <a class="nav-link" href="#get-involved">Get Involved</a>
          </div>
        </div>
      </div>
    </nav>

    <!-- Hero -->
    <main>
      <section class="py-5">
        <div class="container py-5 text-center">
          <h1 class="display-4 fw-bold">Grow biodiversity where you live.</h1>

          <p class="lead mx-auto hero-text">
            Turn your balcony, courtyard or garden into a small green patch
            supporting Melbourne's native biodiversity.
          </p>

          <a href="#plant-finder" class="btn btn-success btn-lg mt-3">
            Find Native Plants
          </a>
        </div>
      </section>

      <!-- Main feature -->
      <section id="plant-finder" class="bg-light py-5">
        <div class="container">
          <div class="text-center mb-5">
            <h2 class="fw-bold">Native Plant Finder</h2>
            <p>
              Tell us about your space and we'll help you find suitable native
              plants.
            </p>
          </div>

          <div class="row g-4">
            <div class="col-12 col-md-4">
              <div class="card h-100 p-3">
                <div class="card-body">
                  <h3 class="h5">1. Your Space</h3>
                  <p class="mb-0">
                    Tell us whether you're planting on a balcony, courtyard or
                    garden.
                  </p>
                </div>
              </div>
            </div>

            <div class="col-12 col-md-4">
              <div class="card h-100 p-3">
                <div class="card-body">
                  <h3 class="h5">2. Growing Conditions</h3>
                  <p class="mb-0">
                    Select the amount of sunlight and available planting area.
                  </p>
                </div>
              </div>
            </div>

            <div class="col-12 col-md-4">
              <div class="card h-100 p-3">
                <div class="card-body">
                  <h3 class="h5">3. Recommendations</h3>
                  <p class="mb-0">
                    Discover native plants suited to your urban space.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>
  </div>
</template>

<<style scoped>
.hero-text {
  max-width: 650px;
}

.card {
  border: 0;
  box-shadow: 0 4px 16px rgba(0, 0, 0, 0.08);
}

@media (max-width: 576px) {
  h1 {
    font-size: 2.2rem;
  }
}
</style>
