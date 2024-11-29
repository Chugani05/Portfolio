<script setup>
    import { useI18n } from "vue-i18n";

    const { locale, t } = useI18n();
</script>

<template>
    <header class="bg-success text-white text-center py-4">
      <h1 class="mb-0">Home</h1>
    </header>

    <section class="container my-5">
        <div class="row">
            <div class="col-md-4 text-center mb-4">
                <figure>
                    <img src="../assets/imgs/book.jpg" class="img-fluid rounded-circle shadow" alt="A picture of my favorite hobby, reading." style="max-width: 250px;">
                </figure>
            </div>
        
            <div class="col-md-8 lead">
                <h2>{{ $t("home-page.h") }}</h2>
                <p>{{ $t("home-page.p") }}</p>

                <div class="icon-container">
                  <a href="https://github.com/Chugani05" target="_blank" class="icon-link" aria-label="GitHub">
                    <i class="bi bi-github"></i>
                  </a>
                  <a href="https://www.linkedin.com/in/tu-perfil/" target="_blank" class="icon-link" aria-label="LinkedIn">
                    <i class="bi bi-linkedin"></i>
                  </a>
                  <a href="https://tu-cv.com" target="_blank" class="icon-link" aria-label="Curriculum Vitae">
                    <i class="bi bi-file-earmark"></i>
                  </a>
                </div>
            </div>
        </div>

      
    </section>
</template>

<style scoped>
  .icon-container {
      display: flex;
      gap: 1.5rem;
      justify-content: center;
      align-items: center;
      margin: 1rem 0;
    }

    .icon-link {
      text-decoration: none;
      color: #333;
      font-size: 2.25rem;
      transition: color 0.3s ease, transform 0.3s ease;
      outline: 3px solid #198754;
      outline-offset: 5px;
    }

    .icon-link:hover {
      color: #198754;
      transform: scale(1.2);
    }
</style>