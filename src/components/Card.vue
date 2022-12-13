<script>
import { def } from '@vue/shared';

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
        flex-basis: 25%;
        padding: 20px;
        // background-color: white;
        // border: solid blue 2px;
        display: flex;
        flex-direction: column;
        cursor: pointer;

        &:hover{
            background-color: $brand_primary;
        }
    }
</style>