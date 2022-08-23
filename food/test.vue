<script setup>
new Vue({
  el: '#app',
  mounted: function(){$('.collapsible').collapsible();},
  data: {
    cards: [
      { title: 'Macaron', src: 'https://res.cloudinary.com/landry-bete/image/upload/v1488769144/dessert14_trnhnj.jpg', description:'Is this thing French ?'},
     { title: 'Tajine', src: 'https://res.cloudinary.com/landry-bete/image/upload/v1525135352/tajine_mfnbd8.jpg', description:'Moroccan people seem to love that dish...'},
      { title: 'Cake', src: 'https://res.cloudinary.com/landry-bete/image/upload/v1525135530/cake_lnh2hn.jpg', description:'Eat healthy my boy!'},
    ]
  }
  })

</script>

<template>
  <div class="row">
  <div class="col l6 m8 s12 offset-m2 offset-l3">
    <ul id="app" class="collapsible popout">
      <li v-for="card in cards" :key="card.title">
        <div class="collapsible-header "><img :src="card.src" class="circle vignette "><span class="headline white--text" v-text="card.title"></span></div>
        <div class="collapsible-body white"><span class="headline white--text" v-text="card.description"></span></div>
      </li>

    </ul>
  </div>
</template>

<style scoped>
a {
  color: #42b983;
}
</style>