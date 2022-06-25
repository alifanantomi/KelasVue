<template>
    <div>

        <h1>{{ tampil }}</h1>

        <ul>
            <li v-for="(item, index) in items" :key="index">
                {{ item.nama }} - Rp{{ item.harga }} - {{ item.kualitas > 70 ? 'Kualitas Tinggi' : 'Kualitas Rendah' }}

            </li>
        </ul>

        <h1 v-if="nilai >= 90">
            Nilai A
        </h1>

        <h1 v-else-if="nilai < 90 && nilai >=75">
            Nilai B
        </h1>

        <h1 v-else>
            Nilai C
        </h1>
    </div>
</template>

<script>
import file from "@/static/file.js"

export default {
    data() {
        return {
            tampil: 'Halo World',
            items: file.arrayProduk,
            nilai: 100
        }
    },
    mounted() { 
        console.log("HOME")  
    }
}
</script>

<style>

</style>