<script>
export default {

    name: "Cards",
    props:["singleComic"]

}
</script>

<template>
    <div class="card col-2 d-flex flex-column align-items-center p-1">
        <figure>
            <img :src="singleComic.thumb" alt="">
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
        aspect-ratio: 1;
    }
    .card p{
        color: white;
        text-align: center;
    }
</style>