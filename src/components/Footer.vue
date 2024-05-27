<!-- SCRIPT -->
<script>
export default {
    data() {
        return {
            items: [
                {
                    title:"DC COMICS",
                    text: ["Characters","Comics","Movies", "TV", "Games", "Videos", "News"],
                    url: [""], 
                },
                {
                    title:"DC",
                    text: ["Terms Of Use","Privacy Policy(New)","Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops","CPSC Certificates", "Ratings", "Shop Help", "Contact Us"],
                    url: [""], 
                },
                {
                    title:"SITES",
                    text: ["DC","MAD Magazine","DC Kids", "DC Universe", "DC Power Visa"],
                    url: [""], 
                },          
                {
                    title:"SHOP",
                    text: ["Shop DC","Shop DC Collectibles"],
                    url: [""], 
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
    <!-- UpperFooter -->
    <div class="row justify-content-center upper_footer">
        <div class="col-8 d-flex ">
            <div class="col-6 text-light d-flex flex-nowrap py-4">
                <div v-for="item, index in items" class="elements_container mx-1">
                    <h3 class="">{{ item.title }}</h3>
                    <p v-for="element,index in items[index].text" class="my-2">
                            {{ element }}
                    </p>
                </div>
            </div>

            <div class="col-6 my_logo_container"></div>
        </div>
    </div>

    <!-- LowerFooter -->
    <div class="row justify-content-center lower_footer">
        <div class="col-8 d-flex py-4">
            <div class="col-3">
                <button class="sign_up_button">SIGN-UP NOW!</button>
            </div>
            <div class="col-9 d-flex justify-content-end align-items-center">
                <div class="col-6 d-flex my_link_container">
                    <p>FOLLOW US</p>
                    <button class="logo_button">
                        <img src="../assets/footer-facebook.png">
                    </button>
                    <button class="logo_button">
                        <img src="../assets/footer-twitter.png">
                    </button>
                    <button class="logo_button">
                        <img src="../assets/footer-youtube.png">
                    </button>
                    <button class="logo_button">
                        <img src="../assets/footer-pinterest.png">
                    </button>
                    <button class="logo_button">
                        <img src="../assets/footer-periscope.png">
                    </button>
                </div>
            </div>
        </div>
    </div>
</template>



<!-- STYLE -->
<style scoped>
    .upper_footer{
        background-image: url(../assets/footer-bg.jpg);
    }
    .elements_container{
        width: 100%;
    }
    .elements_container>p{
        cursor: pointer;
        font-size: 0.8rem;
    }
    
    .my_logo_container{
        background-image: url(../assets/dc-logo-bg.png);
        background-repeat: no-repeat;
        background-position: center;
    }
    .lower_footer{
        background-color: #292929;
    }
    .sign_up_button{
        border: none;
        color: white;
        padding: 16px 32px;
        text-align: center;
        text-decoration: none;
        display: inline-block;
        font-size: 16px;
        margin: 4px 2px;
        transition-duration: 0.4s;
        cursor: pointer;
        background-color: #292929; 
        color: white; 
        border: 3px solid #0D6EFD;
    }
    .sign_up_button:hover {
        background-color: white;
        color: #0D6EFD;
    }

    .my_link_container{
        color: white;
    }
    .my_link_container>p{
        margin: 0.5rem;
        color: #0D6EFD
    }
    .my_link_container>.logo_button{
        border: none;
        color: white;
        border-radius: 50%;
        text-align: center;
        margin: 0px 2px;
        transition-duration: 0.4s;
        cursor: pointer;
        background-color: #292828; 
        color: #080808; 
    }
    .my_link_container .logo_button:hover {
        background-color: white;
        color: #0D6EFD;
    }
    .my_link_container>button>img{
        width: 40px;
    }
</style>
