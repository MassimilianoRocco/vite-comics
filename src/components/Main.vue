<!-- SCRIPT -->
<script>
export default {
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
        }
    },
    methods:{
        getImg(path) {
            let risultato = new URL("../assets/" + path, import.meta.url);
            return risultato.href;
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

    <div class="row bg-dark justify-content-center">
            <div class="content_container col-8">
                <div class="col-12 d-flex align-items-center">
                    <h2>->CONTENT GOES HERE <-</h2>
                </div>
            </div>
        </div>

    <div class="row bg-primary justify-content-center">
        <div class="content_container col-8 d-flex">
            <div v-for="item in items" :href="item.url" class="items_container d-flex align-items-center justify-content-center p-2">
                <div class="col-4 d-flex align-items-center justify-content-center">
                    <img :src="getImg(item.img)">
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
        height: 300px;
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
        left: 15%;
        transform: translateY(50%);
        color: white;
        padding: 0.5rem;
    }
</style>
