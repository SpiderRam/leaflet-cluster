<template>
    <div class="col-sm-8 col-md-2 col-lg-4" id="wrapper">
        <div id="header">Things I learned from this project:</div>
        <ul class="list-group">
            <li class="list-group-item">
                You have to import google fonts into a Vue app, and to pull
                local JSON you place it in a static file, import it, and return
                it in the data function.
            </li>
            <li class="list-group-item">
                It is surprisingly difficult to find/generate/convert sample
                GeoJSON data. The Starbucks theme was entirely driven by the
                data I was able to find and convert from the interwebs.
            </li>
            <li class="list-group-item">
                The town of Tarryall is at the geographical center of Colorado.
            </li>
            <li class="list-group-item">
                The difference between created() and mounted() is significant in
                the creation of a leaflet map in Vue.
            </li>
            <li class="list-group-item">
                This codepen was a fantastic resource, and I am grateful to its
                author:
                <a href="https://codepen.io/xguaita/pen/mJVwwp" target="_blank"
                    >https://codepen.io/xguaita/pen/mJVwwp</a
                >
            </li>
            <li class="list-group-item">
                When you want to build and deploy a simple Vue project to github
                pages, do yourself a big favor and follow this excellent guide:
                <a
                    href="https://dev.to/rolanddoda/deploy-to-github-pages-like-a-pro-with-github-actions-4hdg"
                    >https://dev.to/rolanddoda/deploy-to-github-pages-like-a-pro-with-github-actions-4hdg</a
                >
            </li>
            <li class="list-group-item">
                When I redid this project I did not change much at all from the
                original version. I was on an older version of the Vue CLI and
                the uglify plugin and deprecated loader were killing me on
                deployment. The goal for round two was not to revisit Leaflet,
                but to get this thing deployed. And then, because I have learned
                since I did this the first time that Flexbox is infinitely
                better than Bootstrap, I worked a little on responsiveness.
                Otherwise this is the same as when I first did it 16 months ago
                (around January 2019).
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'app',
    data() {
        return {};
    },
    methods: {},
};
</script>

<style scoped>
#wrapper {
    border: 2px solid forestgreen;
    margin: 1vh auto;
    flex-grow: 1;
    height: 80vh;
    max-width: 49vw;
    min-width: 300px;
    border: 7px transparent;
    padding: 2%;
    background-color: transparent;
}

#header {
    font-family: 'Gaegu', cursive;
    font-size: 1.8em;
}

li {
    font-family: 'Gaegu', cursive;
    font-size: 1.2em;
}

li a {
    overflow-wrap: break-word;
}
</style>
