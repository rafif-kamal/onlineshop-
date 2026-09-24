<script setup>
import { ref, computed } from 'vue'
import ProductCard from '../components/ProductCard.vue'

const daftarProduk = [
  { id: 1, nama: 'Kaos Sekolah', harga: 75000, gambar: '/image/2.jfif' },
  { id: 2, nama: 'Topi Sekolah', harga: 35000, gambar: '/image/1.jfif' },
  { id: 3, nama: 'Tas Sekolah', harga: 120000, gambar: '/image/3.jfif' },
]

const kataKunci = ref('')

const produkTampil = computed(() => {
  const cari = kataKunci.value.trim().toLowerCase()
  if (!cari) return daftarProduk
  return daftarProduk.filter((produk) =>
    produk.nama.toLowerCase().includes(cari)
  )
})
</script>

<template>
  <main>
    <section class="header">
      <h1>Produk Kami</h1>
    </section>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 p-6">
      <ProductCard
        v-for="produk in daftarProduk"
        :key="produk.id"
        :nama="produk.nama"
        :harga="produk.harga"
        :gambar="produk.gambar"
      />
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.header {
  width: 100%;
  padding: 5rem 2rem 1rem;
  text-align: center;
  background: linear-gradient(yellow, white);
  border-radius: 20px;
}

.header h1 {
  font-size: clamp(2rem, 5vw, 3.5rem);
  font-weight: 700;
  letter-spacing: -0.02em;
  line-height: 1.1;
}

.sub {
  margin: 0.25rem 0 2rem;
  color: var(--text-muted);
}
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
  gap: 2rem;
  justify-items: center;
  width: 100%;
}

</style>
