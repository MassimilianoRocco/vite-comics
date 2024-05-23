<!-- SCRIPT -->
<script>
export default {
    data() {
        return {
            links: [
                {
                    text: "CHARACTERS",
                    url: "#characters",
                },
                {
                    text: "COMICS",
                    url: "#comics",
                },
                {
                    text: "MOVIES",
                    url: "#movies",
                },
                {
                    text: "TV",
                    url: "#tv",
                },
                {
                    text: "GAMES",
                    url: "#games",
                },
                {
                    text: "COLLECTIBLES",
                    url: "#collectibles",
                },
                {
                    text: "VIDEOS",
                    url: "#videos",
                },
                {
                    text: "FANS",
                    url: "#fans",
                },
                {
                    text: "NEWS",
                    url: "#news",
                },
                {
                    text: "SHOP",
                    url: "#shop",
                },
            ],
        }
    }
}

</script>



<!-- TEMPLATE HTML -->
<template>
  <div class="row bg-light justify-content-center">
    <div class="col-8 d-flex py-2">
      <div class="col-4">
        <img class="logo" src="../assets/img/dc-logo.png" />
      </div>
      <div class="links_container col-8 d-flex justify-content-end align-items-center text-center">
        <div class="header_links col-1 d-flex justify-content-center align-items-center" v-for="link in links">
          {{ link.text }}
        </div>
      </div>
    </div>
  </div>

</template>



<!-- STYLE -->
<style scoped>

.header_links{
  height: 100%;
  width: calc(100% / 10);

  cursor: pointer;
  font-size: 0.7rem;
  color: black;
}
.header_links:hover{
  border-bottom: 5px solid blue;
}

</style>
