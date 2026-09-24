<script setup>
const props = defineProps(['nama', 'jabatan', 'foto'])
const namaSingkat = props.nama
    .split(' ')
    .map((kata) => kata[0])
    .join('')
    .slice(0, 2)
</script>
<template>
    <div class="kedul">
        <div class="avatar" :style="foto ? { backgroundImage: `url(${foto})` } :  {}">
            <span v-if="!foto">{{ namaSingkat }}</span>
    </div>
    <div class="info">
        <h3>{{ nama }}</h3>
        <p>{{ jabatan }}</p>
    </div>
</div>
</template>
<style scoped>
.kedul {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    gap: 1rem;
    padding: 1rem;
    background: #fff;
    border-radius: 12px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.359);
    text-align: center;
    font-size: 1rem;
}
.avatar {
    width: 80px;
    height: 80px;
    border-radius: 50%;
    background-color: #ccc;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 1.5rem;
    color: #fff;
    background-size: cover;
    background-position: center;
}
.avatar span {
    display:block;
}
.info h3 {
    font-size: 1.2rem;
    font-weight: 600;
    margin: 0;
}
.info p {
    font-size: 1rem;
    color: #666;
    margin: 0;
}
</style>