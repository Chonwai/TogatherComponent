<template>
    <div id="app">
        <section class="flex flex-col items-start">
            <h3>Filter Bar Dropdown Component:</h3>
            <FilterBarDropdown
                @filtering="change"
                :options="testing"
                :row="1"
            />
        </section>
    </div>
</template>

<script lang="ts">
import Vue from 'vue';
import FilterBarDropdown from './components/FilterBarDropdown/FilterBarDropdown';

export default Vue.extend({
    name: 'app',
    data() {
        return {
            testing: [
                '1',
                '2',
                '3',
                '4',
                '5',
                '6',
                '7',
                '8',
                '9',
                '10',
                '11',
                '12',
                '13'
            ]
        };
    },
    components: {
        FilterBarDropdown
    }
});
</script>

<style lang="scss">
#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    padding: 60px;
}
</style>
