<template>
    <h1>Welcome Suon</h1>
    <h4>Project Vue Pertama Saya</h4>
    <h4>Nama Saya {{ nama }}</h4>
    <h4> Umur Saya {{ tahunlahir }} tahun</h4>
    <input v-model="kotalahir" />
    <h5>kota lahir saya : {{ kotalahir }} </h5>
    <button v-on:click="next">next</button>
</template>

<script>
export default {
    data() {
      return{
          nama : "Suon Veasnarithisak",
          tahunlahir : 1998,
          kotalahir : "Phnom Penh, Kamboja"
      }  
    },
    methods:{
        next(){
            this.tahunlahir += 1;
        }
    },
    mounted(){
        this.tahunlahir = 2021 - this.tahunlahir;
    }
}
</script>