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

    <div class="col-8 d-flex py-4">
      <div class="col-4">
        <img class="logo" src="/public/dc-logo.png" />
      </div>
      <div class="links_container col-8 d-flex justify-content-end align-items-center text-center">
        <div v-for="link in links" :href="link.url" class="header_links d-flex justify-content-center align-items-center" >
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
  font-weight: bold;
  color: black;
}
.header_links:hover{
  border-bottom: 5px solid blue;
  color: blue;
}

</style>
