<template>
    <div id="wrapper" class="col-sm-10 col-md-9 col-lg-7">
        <div id="map"></div>
    </div>
</template>

<script>
import starbucksData from '../../static/data/starbucks.json';

export default {
    name: 'app',
    data() {
        return {
            starbucksData,
        };
    },
    methods: {},
    mounted() {
        var self = this;

        var map = L.map('map').setView([39.1219, -105.4756], 7); // eslint-disable-line

        // eslint-disable-next-line
        var baseMap = L.tileLayer(
            'http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
            {
                attribution:
                    '&copy <a href="http://www.openstreetmap.org/copyright" target="_blank">OpenStreetMap</a> contributors',
            }
        ).addTo(map);

        // eslint-disable-next-line
        var points = L.geoJson(null, {
            onEachFeature: function(feature, layer) {
                var location =
                    feature.properties.name != null
                        ? '<strong>' + feature.properties.name + '</strong><br>'
                        : '';
                layer.bindPopup(location);
            },
        });

        function addData() {
            points.addData(self.starbucksData).addTo(map);

            var clusterGroup = L.markerClusterGroup().addLayer(points); // eslint-disable-line

            L.control // eslint-disable-line
                .layers({
                    Clusters: clusterGroup,
                    Stores: points,
                })
                .addTo(map);
        }

        addData();
    },
};
</script>

<style scoped>
#wrapper {
    flex-grow: 1;
    height: 80vh;
    margin: 1vh auto;
    border: 7px ridge forestgreen;
    padding: 2%;
    background-color: limegreen;
    /* box-shadow: 10px 10px 5px grey; */
    max-width: 49vw;
    min-width: 300px;
}

#map {
    height: 100%;
    border: 2px solid forestgreen;
}
</style>
