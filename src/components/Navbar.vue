<script setup>
  import { useI18n } from "vue-i18n";
  // Extraer locale y t desde useI18n
  const { locale, t } = useI18n(); // Esta t es la que usamos en el Template como $t
  // Cambiar el idioma dinámicamente
  const changeLanguage = (lang) => {
  locale.value = lang;
  };
</script>

<template>
  <div class="container-fluid">
    <header class="d-flex flex-wrap justify-content-center py-3 mb-4 border-bottom">
      <a href="/" class="d-flex align-items-center mb-3 mb-md-0 me-md-auto link-body-emphasis text-decoration-none">
        <i class="bi bi-eyeglasses icon-large icon-spacing text-success"></i>
        <span class="fs-4 lead">Rashi Chugani.</span>
      </a>

      <ul class="nav nav-pills">
        <li class="nav-item d-flex align-items-center">
          <RouterLink to="/home" class="text-success">
            <i class="bi bi-house-door-fill icon-medium"></i>
          </RouterLink>
          <RouterLink to="/home" class="nav-link">Home</RouterLink>
        </li>
        <li class="nav-item d-flex align-items-center">
          <RouterLink to="/about" class="text-success">
            <i class="bi bi-star-fill icon-medium"></i>
          </RouterLink>
          <RouterLink to="/about" class="nav-link">{{ $t("aboutme") }}</RouterLink>
        </li>
        <li class="nav-item d-flex align-items-center">
          <RouterLink to="/projects" class="text-success">
            <i class="bi bi-folder-fill icon-medium"></i>
          </RouterLink>
          <RouterLink to="/projects" class="nav-link">{{ $t("projects") }}</RouterLink>
        </li>
        <li class="nav-item d-flex align-items-center">
          <RouterLink to="/skills" class="text-success">
            <i class="bi bi-wrench icon-medium"></i>
          </RouterLink>
          <RouterLink to="/skills" class="nav-link">{{ $t("skills") }}</RouterLink>
        </li>
        <li class="nav-item d-flex align-items-center">
          <RouterLink to="/experience" class="text-success">
            <i class="bi bi-award-fill icon-medium"></i>
          </RouterLink>
          <RouterLink to="/experience" class="nav-link">{{ $t("experience") }}</RouterLink>
        </li>
        <li class="nav-item d-flex align-items-center">
          <RouterLink to="/contact" class="text-success">
            <i class="bi bi-envelope-fill icon-medium"></i>
          </RouterLink>
          <RouterLink to="/contact" class="nav-link">{{ $t("contact") }}</RouterLink>
        </li>

        <div class="btn-group text-success" role="group">
          <button type="button" class="btn btn-outline-success dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">
            <i class="bi bi-translate icon-medium"></i>
          </button>
          <ul class="dropdown-menu">
            <li class="dropdown-item"><a @click="changeLanguage('en')">English</a></li>
            <li class="dropdown-item"><a  @click="changeLanguage('es')">Español</a></li>
          </ul>
        </div>
      </ul>
    </header>
  </div>
</template>

<style scoped>
  .dropdown-item a {
    cursor: pointer;
  }

  .icon-medium {
    font-size: 22px;
  }

  .icon-large {
    font-size: 35px;
  }

  .icon-spacing {
    margin-right: 10px;
    margin-left: 25px;
  }
</style>