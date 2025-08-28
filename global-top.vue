<template>
  <header
    style="
      position: fixed;
      top: 0.5rem;
      right: 1rem;
      width: 180px;
      opacity: 0.8;
      pointer-events: none;
      z-index: 9999;
    "
  >
    <img class="logo" src="/hslu-logos/logo.svg" alt="HSLU Logo" style="width: 100%;" />
  </header>
</template>

<style>
/* Default: no filter */
.logo {
  filter: none;
}

/* When dark mode is active */
.dark .logo {
  filter: invert(1);
}
</style>
