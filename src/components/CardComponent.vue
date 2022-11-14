<template>
    
    <div class="row row-cols-6">
        <div class="col" v-for="(item,index) in characters" :key="index">
            <div class="card" style="width: 10rem;">
                <img :src="item.img" class="card-img-top" :alt="item.name">
                <div class="card-body">
                  <h5 class="card-title">{{item.name}}</h5>
                  <p class="card-text">{{item.occupation}}</p>
                </div>
                <ul class="list-group list-group-flush">
                  <li class="list-group-item">{{item.birthday}}</li>
                  <li class="list-group-item">{{item.status}}</li>
                  <li class="list-group-item">{{item.nickname}}</li>
                </ul>
                <div class="card-body">
                <a href="#" class="card-link">Scopri di più</a>
                </div>
            </div>
        
        </div>
    </div>
    
</template>

<script>
    export default {
        name: 'CardComponents',
        props: ['characters']
    }
</script>

<style lang="scss" scoped>

    img{
        width: 100%;
        aspect-ratio: 1/1.3;
    }

</style>