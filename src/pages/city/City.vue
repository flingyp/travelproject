<template>
  <div>
    <!-- 城市选择-Header -->
    <city-header></city-header>
    <!-- 城市选择-Search -->
    <city-search></city-search>
    <!-- 城市选择-List -->
    <city-list></city-list>
    <!-- 城市选择-Alphabet -->
    <city-alphabet></city-alphabet>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  }
}
</script>

<style lang="stylus" scoped></style>
