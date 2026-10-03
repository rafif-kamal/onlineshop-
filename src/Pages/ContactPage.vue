<template>
    <main>
        <section class="kontak">
            <h1>Kontak Kami</h1>
            <p class="sub">Silakan hubungi kami melalui email atau telepon.</p>
        </section>

        <section class="kontak-content">
            <div class="info">
                <h2>Informasi Kontak</h2>
                <p><span>✉️</span> onlineshop@smkgading.sch.id</p>
                <p><span>📞</span> 0812-3456-7890</p>
                <p><span>📍</span> SMK Gading Island</p>
            </div>

            <form class="form">         
                <label for="nama">Nama</label>
                <input id="nama" type="text" placeholder="Nama lengkap" required />

                <label for="email">Email</label>
                <input id="email" type="email" placeholder="nama@email.com" required />

                <label for="pesan">Pesan</label>
                <textarea id="pesan" rows="4" placeholder="Tulis pesan kamu" required></textarea>

                <button type="submit">Kirim Pesan</button>
            </form>
        </section>
    </main>
</template>

<style scoped>
.kontak {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center; 
  gap: 1rem;
  padding: 5rem 2rem 5rem;
  text-align: center;
  background: linear-gradient(yellow, white);
  border-radius: 20px;
}

.kontak h1 {
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
.kontak-content {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 2rem;
    max-width: 850px;
    margin: 0 auto;
}
@media (max-width: 640px) {
    .kontak-content {
        grid-template-columns: 1fr;
        padding: 0 1rem;
    }
}
.info,
.form {
    display: flex;
    flex-direction: column;
    gap: 0.8rem;
    padding: 1.5rem;
    border: 1px solid var(--border);
    border-radius: var(--radius);
    box-shadow: var(--shadow);
}
.info p {
    color: var(--text-muted);
}
input,
textarea {
    width: 100%;
    box-sizing: border-box;
    padding: 0.7rem;
    border: 1px solid var(--border-dark);
    border-radius: 6px;
    font: inherit;
}
button {
    padding: 0.75rem 1rem;
    border: 0;
    border-radius: 6px;
    background: var(--primary);
    color: white;
    font: inherit;
    font-weight: 600;
    cursor: pointer;
}
button:hover {
    background: var(--primary-dark);
}

</style>