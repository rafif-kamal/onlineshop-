<script setup>
import { ref } from 'vue'
defineProps(['nama', 'harga', 'gambar'])
const gambarDipilih = ref(null)
function bukaPreview(src) {
 gambarDipilih.value = src
}
function tutupPreview() {
 gambarDipilih.value = null
}
function tambahKeKeranjang(nama) {
 const suara = new Audio('/audio/nontifikasi.mp3')
 suara.play()
 alert(`${nama} ditambahkan ke keranjang!`)
}
function beliProduk(nama) {
 alert(`${nama} dipilih untuk dibeli!`)
}
</script>
<template>
 <div class="flex h-full flex-col bg-white rounded-xl shadow-md p-4 hover:shadow-lg transition">
 <img :src="gambar" :alt="nama" @click="bukaPreview(gambar)"
 class="w-full h-40 object-contain rounded-lg cursor-pointer" />
 <h3 class="text-lg font-semibold mt-2">{{ nama }}</h3>
 <p class="text-gray-600">Rp {{ harga.toLocaleString('id-ID') }}</p>
 <div class="flex items-center gap-2 mt-auto pt-2">
 <button @click="beliProduk(nama)"
 class="flex-1 bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700">
 Beli
 </button>
 <button @click="tambahKeKeranjang(nama)"
 class="bg-blue-600 text-white px-3 py-2 text-sm rounded-lg hover:bg-blue-700 whitespace-nowrap">
 🛒
 </button>
 </div>
 </div>
 <div v-if="gambarDipilih" class="fixed inset-0 bg-black/70 flex items-center justify-center cursor-zoom-out"
 @click="tutupPreview">
 <img :src="gambarDipilih" class="max-w-[80%] max-h-[80%] rounded-lg" />
 </div>
</template>