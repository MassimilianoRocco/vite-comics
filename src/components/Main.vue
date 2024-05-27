<!-- SCRIPT -->
<script>
import Cards from "./Cards.vue";

export default {

    components: {
        Cards
    },

    data() {
        return {
            items: [
                {
                    img: "buy-comics-digital-comics.png", 
                    text: "DIGITAL COMICS",
                    url:"",
                },
                {
                    img: "buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                    url:"",
                },
                {
                    img: "buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION",
                    url:"",
                },
                {
                    img: "buy-comics-shop-locator.png",
                    text: "COMIC SHOP LOCATOR",
                    url:"",
                },
                {
                    img: "buy-dc-power-visa.svg",
                    text: "DC POWER VISA",
                    url:"",
                },
                
            ],

            fumetti: [
                {
                    thumb: "https://www.coverbrowser.com/image/action-comics/1-1.jpg",
                    price: "$19.99",
                    series: "Action Comics",
                    type: "comic book",
                },
                {
                    thumb: "https://www.panini.it/media/catalog/product/cache/a5b5dd3adfe0d321084804c738f29601/M/1/M1BLLA015ISBN_0.jpg",
                    price: "$3.99",
                    series: "American Vampire 1976",
                    type: "comic book",
                },
                {
                    thumb: "https://media.wired.com/photos/593384dad80dd005b42b2817/master/w_2560%2Cc_limit/Aquaman-16.jpg",
                    price: "$16.99",
                    series: "Aquaman",
                    type: "graphic novel",
                },
                {
                    thumb: "https://d29xot63vimef3.cloudfront.net/image/batgirl/1-1.jpg",
                    price: "$2.99",
                    series: "Batgirl",
                    type: "comic book",
                },
                {
                    thumb: "https://static.posters.cz/image/750/locandine-film-in-plexiglass-batman-prowl-comic-cover-i69653.jpg",
                    price: "$3.99",
                    series: "Batman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/50/Batman_Beyond_v.1_1.jpg",
                    price: "$2.99",
                    series: "Batman Beyond",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/0/0d/Batman_Superman_Vol_1_1.jpg",
                    price: "$3.99",
                    series: "Batman/Superman",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/cf/Batman_Superman_Annual_Vol_2_1.jpg",
                    price: "$4.99",
                    series: "Batman/Superman Annual",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/5/54/Batman_The_Joker_War_Zone_Vol_1_1.jpg",
                    price: "$5.99",
                    series: "Batman: The Joker War Zone",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/6/64/Batman_Three_Jokers_Collected.jpg",
                    price: "$6.99",
                    series: "Batman: Three Jokers",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/f/f8/Batman_White_Knight_Presents_Harley_Quinn_Vol_1_1.jpg",
                    price: "$4.99",
                    series: "Batman: White Knight Presents: Harley Quinn",
                    type: "comic book",
                },
                {
                    thumb: "https://static.wikia.nocookie.net/marvel_dc/images/c/c8/Catwoman_Vol_2_1.jpg",
                    price: "$16.99",
                    series: "Catwoman",
                    type: "graphic novel",
                },
            ],
        }
    },
    methods:{
        getImage(nomefile) {
            return new URL(`../assets/${nomefile}`, import.meta.url);
        },
    }
}

</script>



<!-- TEMPLATE HTML -->
<template>
    <div class="jumbo_container row position-relative justify-content-center">
        <div class="content_title_box text-center bg-primary">
            CURRENT SERIES
        </div>
    </div>

    <!-- IMPORTO/UTILIZZO IL COMPONENTE CARDS -->
    <div class="fluid-container">
        <div class="row bg-dark justify-content-center position-relative">
            <div class="content_container col-8 d-flex flex-wrap">
                <Cards v-for="elemento in fumetti" :singleComic="elemento"/>
            </div>
            <div class="loadMore_Box text-center bg-primary">
                LOAD MORE
            </div>
        </div>
    </div>


    <div class="row bg-primary justify-content-center">
        <div class="content_container col-8 d-flex">
            <div v-for="item in items" :href="item.url" class="items_container d-flex align-items-center justify-content-center p-2">
                <div class="col-4 d-flex align-items-center justify-content-center">
                    <img :src="getImage(item.img)">
                </div>
                <div class="col-8 d-flex align-items-center ms-2">
                    <p>{{ item.text }}</p>
                </div> 
            </div>
        </div>
    </div>
        
    

</template>



<!-- STYLE -->
<style scoped>
    .jumbo_container{
        height: 400px;
        background-image: url(../assets/jumbotron.jpg);
        background-size: cover;
    }
    .content_container{
        padding: 4rem 0;
    }

    h2{
        color: white;
    }

    .items_container{
        width: calc(100% / 5);
        color: white;
        cursor: pointer;
    }
    img{
       width: 60px;
       aspect-ratio: 1;
    }

    .content_title_box{
        width: 150px;
        position: absolute;
        bottom: 0;
        left: 17%;
        transform: translateY(50%);
        color: white;
        padding: 0.5rem;
        z-index: 999;
    }
    .loadMore_Box{
        width: 150px;
        position: absolute;
        bottom: 2%;
        color: white;
        padding: 0.5rem;
    }
</style>
