<template>
  <div>
    <!-- 城市选择-Header -->
    <city-header></city-header>
    <!-- 城市选择-Search -->
    <city-search></city-search>
    <!-- 城市选择-List -->
    <city-list :cities="cities" :hot="hotCities"></city-list>
    <!-- 城市选择-Alphabet -->
    <city-alphabet :cities="cities"></city-alphabet>
  </div>
</template>

<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/List'
import CityAlphabet from './components/Alphabet'
import axios from 'axios'
export default {
  name: 'City',
  components: {
    CityHeader,
    CitySearch,
    CityList,
    CityAlphabet
  },
  data() {
    return {
      hotCities: [],
      cities: {}
    }
  },
  methods: {
    getCityInfo() {
      axios.get('/api/city.json').then(this.handleGetCityInfoSucc)
    },
    handleGetCityInfoSucc(res) {
      console.log(res)
      res = res.data
      // 如果返回的是true 或者 有数据
      if (res.ret && res.data) {
        const data = res.data
        this.cities = data.cities
        this.hotCities = data.hotCities
      }
    }
  },
  mounted() {
    this.getCityInfo()
  }
}
</script>

<style lang="stylus" scoped></style>
