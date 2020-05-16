<template>
    <div class="header">
        <div class="innerContainer">
            <div class="title">Leaflet.js Map</div>
            <p class="subtitle">
                Learning the basics of leaflet, and practicing with Vue
                components.
            </p>
        </div>
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
.header {
    font-family: 'Gaegu', cursive;
    margin-bottom: 5%;
    background-image: url('../images/trianglify-green.png');
    text-shadow: 1px 1px 2px black, 0 0 25px lemonchiffon, 0 0 5px lawngreen;
    background-size: cover;
    width: 100vw;
    height: 230px;
}

.title {
    font-size: 4em;
}

.innerContainer {
    margin: 0 3vw;
}

.subtitle {
    font-size: 2em;
}
</style>
