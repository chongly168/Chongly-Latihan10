<template>
  <Title title="Catatan pengeluaran"/>
  <FormMahasiswa @entri-mahasiswa = "entriMahasiswa($event)"/>
  <ListMahasiswa v-if="dataMahasiswa.length>0" :dataMahasiswalist="dataMahasiswa"/>
</template>

<script>
import Title from './components/Title.vue'
import FormMahasiswa from './components/FormMahasiswa.vue'
import ListMahasiswa from './components/ListMahasiswa.vue'
export default {
  name: 'App',
  components: {
    Title,
    ListMahasiswa,
    FormMahasiswa,
  },
  data(){
    return{
      dataMahasiswa : [
        {nim : 'D112012118', nama : 'Dos Chongly', kelas : 'IF18-B'}
        
      ],
    }
  },
  methods:{
    entriMahasiswa(event){
      this.dataMahasiswa.push(event);
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>