<template>
  <main>
    <section class="hero">
      <h1>Selamat Datang di Onlineshop SMKN 1 Gading </h1>
      <p>Belanja kebutuhan sekolah jadi gampang, belajar jadi senang.</p>
      <RouterLink to="/product" class="tomol">Lihat Produk</RouterLink>
    </section>
    <video controls muted loop>
 <source src="/video/promo-toko.mp4" type="video/mp4" />
 Browser kamu tidak mendukung pemutaran video.
 </video>
    <div class="hayam">
     <div class="item">
        <span class="emoji">💰</span>
        <h2>Harga Mejeuh</h2>
        <p>aman da moal boncos, sok geura meser.</p>
      </div>
      <div class="item">
        <span class="emoji">🚚</span>
        <h2>Di Anteurkeun</h2>
        <p>dagoan weh pokonamah engke jol aya harepeun benget.</p>
      </div>
      <div class="item">
        <span class="emoji">⭐</span>
        <h2>Kualitas Mejeuh</h2>
        <p>soksok lah meuli.</p>
      </div>
      </div>
  </main>
</template>

<style scoped>
main {
  display: flex;
  flex-direction: column;
  gap: 3rem;
}

.hero h1 {
  font-size: clamp(2rem, 5vw, 3.5rem);
  font-weight: 700;
  letter-spacing: -0.02em;
  line-height: 1.1;
}

video {
 margin-top: 16px;
 border-radius: 10px;
 display: block;
 width: 100%;
 max-width: 720px;
 height: auto;
 aspect-ratio: 16 / 9;
 object-fit: contain;
 margin-left: auto;
 margin-right: auto;
}

.hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 1.25rem;
  padding: 5rem 2rem 5rem;
  text-align: center;
  background: linear-gradient(yellow, white);
  border-radius:  20px;
}
.hayam {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 1rem;
  align-items: stretch;
}

.tomol {
  margin-top: 1rem;
  padding: 0.85rem 2.5rem;
  border-radius: 999px;
  background:white;
  color: #212020;
  font-weight: 600;
  transition: background-color 0.2s;
}

.tomol:hover {
  background: yellow;
  transform: translateY(-5px);
}
.item {
  display: flex; gap: 1rem; flex-wrap: wrap; 
  flex-direction: column;
  justify-content: center;
  gap: 1rem;
  padding: 1rem;
  background: #fff;
  border-radius: 12px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.359);
  text-align: center;
  font-size: 1rem;
}

.emoji {
  font-size: 1.75rem;
}
</style>
