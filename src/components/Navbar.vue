<template>
  <header class="navbar">
    <RouterLink to="/" class="brand">
      <strong>SMK Gading Island</strong>
      <small>Onlineshop Sekolah</small>
    </RouterLink>
    <nav>
      <RouterLink to="/">Beranda</RouterLink>
      <RouterLink to="/product">Produk</RouterLink>
      <RouterLink to="/about">Tentang</RouterLink>
      <RouterLink to="/contact">Kontak</RouterLink>
    </nav>
  </header>
</template>

<style scoped>
.navbar {
  position: sticky;
  top: 0;
  z-index: 100;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 1rem;
  padding: 1.1rem 2rem;
  background: var(--bg);
  border-bottom: 1px solid var(--border);
  background: linear-gradient(rgb(242, 242, 240), yellow);
}

.brand {
  display: flex;
  flex-direction: column;
  line-height: 1.3;
  color: var(--text);
}

.brand strong {
  font-size: 1.05rem;
  font-weight: 700;
  letter-spacing: -0.01em;
}

.brand small {
  color: var(--text-muted);
  font-size: 0.8rem;
}

nav {
  display: flex;
  gap: 0.25rem;
}

nav a {
  position: relative;
  padding: 0.5rem 1rem;
  color: black;
  font-weight: 500;
  transition: color 0.2s;
}

nav a:hover {
  color: rgb(254, 254, 253);
}

nav a.router-link-active {
  color: var(--text);
  font-weight: 600;
  background: rgb(255, 255, 255);
  border-radius: 20px;
}

nav a.router-link-active::after {
  transform: scaleX(1);
}

@media (max-width: 640px) {
  .navbar {
    flex-direction: column;
    gap: 0.75rem;
  }

  .brand small {
    display: none;
  }
}
</style>
