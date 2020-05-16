<template>
  <div class="col-sm-8 col-md-2 col-lg-4" id="wrapper">
    <div id="header">Things I learned from this project:</div>
    <ul class="list-group">
      <li class="list-group-item">You have to import google fonts into a Vue app, and to pull local JSON you place it in a static file, import it, and return it in the data function.</li>
      <li class="list-group-item">It is surprisingly difficult to find/generate/convert sample GeoJSON data.  The Starbucks theme was entirely driven by the data I was able to find and convert from the interwebs.</li>
      <li class="list-group-item">The town of Tarryall is at the geographical center of Colorado.</li>
      <li class="list-group-item">The difference between created() and mounted() is significant in the creation of a leaflet map in Vue.</li>
      <li class="list-group-item">This codepen was a fantastic resource, and I am grateful to its author:  <a href="https://codepen.io/xguaita/pen/mJVwwp" target="_blank">https://codepen.io/xguaita/pen/mJVwwp</a></li>
    </ul>
  </div>
</template>


<script>
export default {
  name: 'app',
  data () {
    return {

    }
  },
  methods: {

  }
}
</script>

<style scoped>

  #wrapper {
    float: right;
    padding-top: 1%;
    border: 2px solid forestgreen;
    margin-right: 2.5%;
  }

  #header {
    font-family: 'Gaegu', cursive;
    font-size: 1.8em;
  }

  li {
    font-family: 'Gaegu', cursive;
    font-size: 1.2em;
  }

</style>
