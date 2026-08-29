<script setup>
import { ref } from 'vue'

const spaceType = ref('')
const sunlight = ref('')
const plantingArea = ref(null)
const errorMessage = ref('')

const submitSpaceQuiz = () => {
  if (spaceType.value === '') {
    errorMessage.value = 'Please select a space type.'
    return
  }

  if (sunlight.value === '') {
    errorMessage.value = 'Please select the amount of sunlight.'
    return
  }

  if (!plantingArea.value || plantingArea.value < 1 || plantingArea.value > 100) {
    errorMessage.value = 'Planting area must be between 1 and 100 m².'
    return
  }

  errorMessage.value = ''

  console.log('Space type:', spaceType.value)
  console.log('Sunlight:', sunlight.value)
  console.log('Planting area:', plantingArea.value)
}
</script>

<template>
  <div>
    <nav class="navbar navbar-expand-lg navbar-dark bg-success">
      <div class="container">
        <a class="navbar-brand fw-bold" href="#home">
          Patch Melbourne
        </a>

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

    <main>
      <section id="home" class="hero-section">
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
        <div class="container">
          <div class="text-center mb-5">
            <h2 class="fw-bold">Native Plant Finder</h2>

            <p class="text-muted">
              Tell us about your space and we'll help you find
              suitable Melbourne native plants.
            </p>
          </div>

          <div class="row justify-content-center">
            <div class="col-12 col-md-9 col-lg-7">
              <div class="card border-0 shadow-sm">
                <div class="card-body p-4 p-md-5">
                  <h3 class="h4 fw-bold mb-4">
                    Tell us about your space
                  </h3>

                  <form @submit.prevent="submitSpaceQuiz">
                    <div class="mb-4">
                      <label
                        for="spaceType"
                        class="form-label fw-semibold"
                      >
                        What type of space do you have?
                      </label>

                      <select
                        id="spaceType"
                        v-model="spaceType"
                        class="form-select"
                      >
                        <option value="">Select your space</option>
                        <option value="balcony">Balcony</option>
                        <option value="courtyard">Courtyard</option>
                        <option value="garden">Garden</option>
                      </select>
                    </div>

                    <div class="mb-4">
                      <label
                        for="sunlight"
                        class="form-label fw-semibold"
                      >
                        How much sunlight does the space receive?
                      </label>

                      <select
                        id="sunlight"
                        v-model="sunlight"
                        class="form-select"
                      >
                        <option value="">Select sunlight</option>
                        <option value="full">Full sun</option>
                        <option value="partial">Partial sun</option>
                        <option value="shade">Mostly shade</option>
                      </select>
                    </div>

                    <div class="mb-4">
                      <label
                        for="plantingArea"
                        class="form-label fw-semibold"
                      >
                        Available planting area (m²)
                      </label>

                      <input
                        id="plantingArea"
                        v-model.number="plantingArea"
                        type="number"
                        class="form-control"
                        min="1"
                        max="100"
                        placeholder="e.g. 5"
                      />

                      <div class="form-text">
                        Enter an area between 1 and 100 m².
                      </div>
                    </div>

                    <div
                      v-if="errorMessage"
                      class="alert alert-danger"
                    >
                      {{ errorMessage }}
                    </div>

                    <button
                      type="submit"
                      class="btn btn-success btn-lg w-100"
                    >
                      Find My Plants
                    </button>
                  </form>
                </div>
              </div>
            </div>
          </div>
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

#find-plants {
  min-height: 70vh;
}

.card {
  border-radius: 16px;
}

.form-control,
.form-select {
  min-height: 48px;
}

@media (max-width: 992px) {
  .hero-section {
    min-height: 60vh;
  }
}

@media (max-width: 576px) {
  .hero-section {
    min-height: 55vh;
    padding: 3rem 1rem;
  }

  .hero-section h1 {
    font-size: 2.2rem;
  }

  .hero-description {
    font-size: 1rem;
  }

  #find-plants {
    padding-left: 0.5rem;
    padding-right: 0.5rem;
  }
}
</style>