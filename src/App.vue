<template>
    <div id="app">
        <app-header></app-header>
        <div class="row">
            <app-title></app-title>
        </div>
        <div class="row">
            <app-map></app-map>
            <app-sidebar></app-sidebar>
        </div>
    </div>
</template>

<script>
import MapVue from './components/Map.vue';
import HeaderVue from './components/Header.vue';
import SidebarVue from './components/Sidebar.vue';
import TitleVue from './components/Title.vue';

export default {
    name: 'app',
    data() {
        return {};
    },
    components: {
        appMap: MapVue,
        appHeader: HeaderVue,
        appSidebar: SidebarVue,
        appTitle: TitleVue,
    },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Gaegu:300');

.row {
    margin-bottom: 5%;
}
</style>
