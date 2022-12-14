<script>

    export default{
        props:{
            details: Object,
        }
    }
</script>

<template>
    <!-- Creare la struttura della card -->
    <div class="card">
        <img :src="details.thumb" alt="">
        <h3>{{details.series}}</h3>
    </div>
</template>

<style lang="scss" scoped>
    @use '../styles/general.scss' as *;
    .card{
        flex-basis: calc(100% / 6 - 20px);
        display: flex;
        flex-direction: column;
        cursor: pointer;
        &:hover{
            background-color: $brand_primary;
        }

        & h3{
            padding-top: 10px;
        }
    }
</style>