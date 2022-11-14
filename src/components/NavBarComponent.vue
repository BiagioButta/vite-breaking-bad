<template>
    <div class="row">
        <div class="col"><h1>Trovati {{characters.length}} personaggi</h1></div>
    </div>
</template>

<script>
    export default {
        name: 'NavBarComponent',
        props: ['characters']
    }
</script>

<style lang="scss" scoped>

</style>