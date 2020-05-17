<template>
    <div>
        <p class="title">All Starbucks Locations in the State of Colorado.</p>
        <p class="subtitle close">
            (Well, pretty close; I'm sure there are more now....)
        </p>
        <p class="subtitle">
            Select the 'Clusters' view for a more user-friendly map.
        </p>
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
div {
    margin: 0 auto;
    width: 70%;
    text-align: center;
    font-family: 'Gaegu', cursive;
}

.title {
    font-size: 3em;
    margin-bottom: 5px;
}

.subtitle {
    font-size: 2em;
}

.close {
    margin-top: 10px;
    font-size: 1.5em;
}
</style>
