<script>
export default {

    name: "Cards",
    props:["singleComic"],

    // OPPURE, MEGLIO...
    // props:{
    //     elemento: "singleComic"
    // }

    data() {
            return {
            }
        },
        methods:{
            getImage(nomefile) {
                return new URL(`../assets/${nomefile}`, import.meta.url);
            }
        }
}
</script>

<template>
    <div class="card col-2 d-flex flex-column align-items-center p-1">
        <figure>
            <img :src= "singleComic.thumb" alt="">
        </figure>
        <p>{{ singleComic.series }}</p>
    </div>
</template>

<style>

    .card{
        background-color: rgb(33, 37, 41);
    }

    .card img{
        width: 100%;
        object-fit: cover;
        aspect-ratio: 9 / 16;
    }
    .card p{
        color: white;
        text-align: center;
    }
</style>