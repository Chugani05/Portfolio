<script setup>
  import { useI18n } from "vue-i18n";
  // Extraer locale y t desde useI18n
  const { locale, t } = useI18n(); // Esta t es la que usamos en el Template como $t
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

                <div class="icon-large icon-spacing">
                  <a href="https://github.com/Chugani05"><i class="bi bi-github"></i></a>
                  <i class="bi bi-linkedin"></i>
                  <i class="bi bi-file-earmark"></i>
                </div>
            </div>
        </div>

      
    </section>
</template>

<style scoped>
  .icon-large {
    font-size: 30px;
  }

  .icon-spacing {
    margin-right: 10px;
    margin-left: 10px;
  }
</style>