<script setup>
import TeamCard from '../components/TeamCard.vue'

const daftarTim = [
  {
    id: 1,
    nama: 'lutfi',
    jabatan: 'Ketua Tim',
  },
  {
    id: 2,
    nama: 'danar',
    jabatan: 'Anggota Tim',
  },
  {
    id: 3,
    nama: 'david disini',
    jabatan: 'Anggota Tim',
  },
]
</script>
<template>
  <main>
    <div class="hebrot">
      <h1>Tentang Kami</h1>
      <p class="sub">
        Onlineshop ini dikelola oleh siswa SMK Gading Island jurusan PPLG.
      </p>
    </div>
    <div class="cerita">
      <div class="hay">
        <h2>Cerita Dibalik Onlineshop</h2>
        <p>
          Onlineshop ini dibuat untuk memenuhi tugas akhir mata pelajaran PPLG.
          Onlineshop ini dibuat menggunakan Vue.js dan Tailwind CSS. Onlineshop ini
          juga menggunakan Firebase sebagai backendnya.
        </p>
      </div>
      <div class="foto">
        <img src="/image/images.jfif" alt="Foto Tim" />
      </div>
    </div>
    <div class="tim">
      <TeamCard
        v-for="anggota in daftarTim"
        :key="anggota.id"
        :nama="anggota.nama"
        :jabatan="anggota.jabatan"
      />
    </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}
.hebrot {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 1rem;
  padding: 5rem 2rem 5rem;
  text-align: center;
  background: linear-gradient(yellow, white);
  border-radius:  20px;
}

h1 {
  font-size: clamp(2rem, 5vw, 3.5rem);
  font-weight: 700;
  letter-spacing: -0.02em;
  line-height: 1.1;
}

.sub {
  max-width: 60ch;
  color: var(--text-muted);
  font-size: 1.2rem;
  text-align: center;
}
.tim {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 1rem;
  align-items: stretch;
}
.cerita {
  display: flex;
  align-items: stretch;
  justify-content: space-between;
  margin: 20px 50px;
  gap: 30px;
}
.hay,
.foto {
  flex: 1;
  min-width: 0;
}
.hay {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  padding: 1rem;
}
.foto {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1rem;
}
.foto img {
  width: 100%;
  aspect-ratio: 4 / 3;
  object-fit: cover;
  border-radius: 12px;
}

@media (max-width: 768px) {
  .cerita {
    flex-direction: column;
    margin: 20px 0;
  }
}
</style>
