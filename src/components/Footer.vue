<script setup>
const tahun = new Date().getFullYear()
</script>

<template>
  <footer class="footer">
    <p>&copy; {{ tahun }} SMK Gading Island — Onlineshop Sekolah</p>
    <p class="sub">Dikelola oleh siswa jurusan PPLG</p>
  </footer>
</template>


<style scoped>
.footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 0.35rem;
  padding: 2.5rem 1.5rem;
  background: #fafafa;
  border-top: 1px solid var(--border);
  color: var(--text-muted);
  text-align: center;
  font-size: 0.95rem;
}

.footer .sub {
  font-size: 0.85rem;
  color: var(--text-muted);
}
</style>
