<template lang="html">
  <div v-if="film" class="info-container">
    <h1>{{film.title}}</h1>
    <div class="box-description">
      <h4>{{film.description}}</h4>
    </div>
    <div class="box-info">
      <p><b>Director:</b> {{film.director}}</p>
      <p><b>Producer:</b> {{film.producer}}</p>
      <p><b>Realase Date:</b> {{film.release_date}}</p>
    </div>

    <template v-if="film.title === 'Castle in the Sky'">
      <img src="https://images.alphacoders.com/828/thumb-1920-828255.png">
    </template>
    <template v-if="film.title === 'My Neighbor Totoro'">
      <img src="https://i.pinimg.com/originals/c0/45/58/c045589789eccc907c6959a2e7641d54.jpg">
    </template>
    <template v-if="film.title === 'Kikis Delivery Service'">
      <img src="https://www.google.com/imgres?imgurl=https%3A%2F%2Fthewellredmage.files.wordpress.com%2F2016%2F12%2Fkiki-pos_1440449334.png%3Fw%3D500&imgrefurl=https%3A%2F%2Fthewellredmage.com%2F2016%2F12%2F11%2Fkikis-delivery-service%2F&docid=Ww8YtVgCpOW-XM&tbnid=Nywkj54DkAkcqM%3A&vet=10ahUKEwjonf-c3dTgAhVuwMQBHZCKAKUQMwioAShNME0..i&w=500&h=750&bih=710&biw=1386&q=Kiki%27s%20Delivery%20Service%20hd&ved=0ahUKEwjonf-c3dTgAhVuwMQBHZCKAKUQMwioAShNME0&iact=mrc&uact=8">
    </template>
    <template v-if="film.title === 'Only Yesterday'">
      <img src="https://ic.c4assets.com/brands/only-yesterday/a88e3d6d-e6e6-4c8d-9b7e-a80a25b1861e.jpg?interpolation=progressive-bicubic&output-quality=90">
    </template>
    <template v-if="film.title === 'Grave of the Fireflies'">
      <img src="https://keithandthemovies.files.wordpress.com/2017/12/graveposter.jpg?w=545">
    </template>
    <template v-if="film.title === 'Porco Rosso'">
      <img src="http://barkerhost.com/wp-content/uploads/sites/4/2016/06/porco-banner.jpg">
    </template>
    <template v-if="film.title === 'Pom Poko'">
      <img src="https://fanart.tv/fanart/movies/15283/hdmovieclearart/pom-poko-54ea2a3f639e1.png">
    </template>
    <template v-if="film.title === 'Whisper of the Heart'">
      <img src="https://m0.joe.co.uk/wp-content/uploads/2018/07/25164315/ce196d896889ce984b8c36f6c8ed64b0.jpg">
    </template>
    <template v-if="film.title === 'Princess Mononoke'">
      <img src="https://backtotheviewer.files.wordpress.com/2015/11/princess-mononoke.jpg?w=640">
    </template>
    <template v-if="film.title === 'My Neighbors the Yamadas'">
      <img src="https://entropymag.org/wp-content/uploads/2015/03/series_1484.jpg">
    </template>
    <template v-if="film.title === 'Spirited Away'">
      <img src="https://cdn.hitc-s.com/i/189/spirited_away_wallpaper_by_behruz_78544.jpg">
    </template>
    <template v-if="film.title === 'The Cat Returns'">
      <img src="https://s1.thcdn.com/productimg/1600/1600/11655841-9754546298583822.jpg">
    </template>
    <!-- <template v-if='film.id === "cd3d059c-09f4-4ff3-8d63-bc765a5184fa"'>
      <img src="https://www.goog6_c1081.0021.jpg&imgrefurl=http%3A%2F%2Fwww.ifccenter.com%2Ffilms%2Fhowls-moving-castle%2F&docid=hXrWW_t0hSUscM&tbnid=XEPERK_yhbWzQM%3A&vet=10ahUKEwiN8rni5dTgAhV1unEKHWlpDfQQMwhCKAUwBQ..i&w=2218&h=1200&bih=710&biw=1386&q=Howl%27s%20Moving%20Castle&ved=0ahUKEwiN8rni5dTgAhV1unEKHWlpDfQQMwhCKAUwBQ&iact=mrc&uact=8"> -->
    <!-- </template> -->
    <template v-if="film.title === 'Tales from Earthsea'">
      <img src="https://filmschoolrejects.com/wp-content/uploads/2018/05/tales-from-earthsea.png">
    </template>
    <template v-if="film.title === 'Ponyo'">
      <img src="http://images2.fanpop.com/image/photos/11000000/Ponyo-ponyo-on-the-cliff-by-the-sea-11063832-1280-1024.jpg">
    </template>
    <template v-if="film.title === 'Arrietty'">
      <img src="https://m.media-amazon.com/images/M/MV5BMTAxNjk3OTYyODReQTJeQWpwZ15BbWU3MDgyODY2OTY@._V1_.jpg">
    </template>
    <template v-if="film.title === 'From Up on Poppy Hill'">
      <img src="https://www.nziff.co.nz/assets/resized/sm/upload/vf/48/ah/ai/Poppy%20Hill%20NEW%20KEY%20c0349_t2JPEG.0082-2000-2000-1125-1125-crop-fill.jpg">
    </template>
    <template v-if="film.title === 'The Wind Rises'">
      <img src="https://i.ytimg.com/vi/RzSpDgiF5y8/maxresdefault.jpg">
    </template>
    <template v-if="film.title === 'The Tale of the Princess Kaguya'">
      <img src="https://cdn-static.denofgeek.com/sites/denofgeek/files/styles/main_wide/public/0/21/kaguya-main.jpg?itok=LIRawTR3">
    </template>
    <template v-if="film.title === 'When Marnie Was There'">
      <img src="https://ic.c4assets.com/bips/when-marnie-was-there/articles/931b0b3a-b75f-40e1-af60-16510f8ec547.jpg?interpolation=progressive-bicubic&output-quality=90">
    </template>


  </div>
</template>

<script>
export default {
  name: 'film-details',
  props: ['film'],

}
</script>

<style lang="css" scoped>

img {
  width:500px;
  height:300px;
  display: flex;
  margin: 20px;
  border-radius: 5%
}

h1 {
  font-family: fantasy;
  font-weight: bold;
  display: center;
  background-color: white;
  border: 1px solid white;
  opacity: 0.9;
  width: 600px;
  padding: 10px;
  margin: 20px;
  border-radius: 10%;
}

p {
  font-family: "Courier New", Courier, monospace;
}

h4 {
  font-family: "Courier New", Courier, monospace;
  font-weight: lighter;
  font-size: 18px;
}

.box-description, .box-info {
  display: flex;
  background-color: white;
  border: 1px solid white;
  opacity: 0.9;
  width: 600px;
  padding: 10px;
  margin: 20px;
  border-radius: 10%;
}



</style>
