<template>
    <div class="top">
        <h1>{{title}}</h1>
        <hr>
    </div>
</template>

<script>
export default {
    name: 'HeaderNav',
    data() {
        return {
            title: 'Filmes em Cartaz'
        }
    }
}
</script>

<style lang="scss">
.top {
    min-width: 400px;

    h1 {
    padding: 30px;
}
}

</style>