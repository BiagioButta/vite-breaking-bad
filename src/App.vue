<template>
  <div class="container debug">
    <div class="row">
      <div class="col debug"><NavBarComponent :characters="characterList" /></div>
      <div class="col debug"><SearchComponent/></div>
    </div>
    <div class="row"><div class="col"><CardComponent :characters="characterList" /></div></div>
  </div>
</template>

<script>

  import axios from 'axios';
  import NavBarComponent from './components/NavBarComponent.vue';
  import CardComponent from './components/CardComponent.vue';
  import SearchComponent from './components/SearchComponent.vue';

  export default {
    components: {
      NavBarComponent,
      CardComponent,
      SearchComponent
    },
    data() {
      return {
        apiURL: 'https://www.breakingbadapi.com/api/characters',
        characterList: []
      }
    },
    methods: {
      getCharacters(){
        axios.get(this.apiURL).then(
          (res)=>{
            this.characterList = [...res.data]
            console.log(this.characterList)
          }
        )
      }
    },
    created(){
      this.getCharacters()
    }
  }
</script>

<style lang="scss" scoped>

</style>