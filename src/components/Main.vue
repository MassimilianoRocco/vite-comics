<!-- SCRIPT -->
<script>
export default {
    data() {
        return {
            items: [
                {
                    img: "public/buy-comics-digital-comics.png", 
                    text: "DIGITAL COMICS",
                    url:"",
                },
                {
                    img: "public/buy-comics-merchandise.png",
                    text: "DC MERCHANDISE",
                    url:"",
                },
                {
                    img: "public/buy-comics-subscriptions.png",
                    text: "SUBSCRIPTION",
                    url:"",
                },
                {
                    img: "public/buy-comics-shop-locator.png",
                    text: "COMIC SHOP LOCATOR",
                    url:"",
                },
                {
                    img: "public/buy-dc-power-visa.svg",
                    text: "DC POWER VISA",
                    url:"",
                },
                
            ],
        }
    }
}

</script>



<!-- TEMPLATE HTML -->
<template>
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
                    <img :src="item.img">
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
</style>
