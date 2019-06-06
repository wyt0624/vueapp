<template>
    <div>
        <city-header></city-header>
        <city-search></city-search>
        <city-list></city-list>
    </div>
</template>
<script>
import CityHeader from "./conponents/Header"
import CitySearch from "./conponents/Search"
import CityList from "./conponents/List"

export default {
    name: "City",
    components: {
        CityHeader,
        CitySearch,
        CityList,
    }
}
</script>
<style lang="stylus" scoped>
    
</style>