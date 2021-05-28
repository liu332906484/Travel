<template>
   <div class="city">
     <city-header></city-header>
     <city-search></city-search>
     <city-list :Cityposition = 'Cityposition' :hotCities = 'hotCities' :cities = 'cities' :letter = 'letter'></city-list>
     <side-nav :cities = 'cities' @change= 'handLetterChang'></side-nav>
   </div>
</template>

<script>
import CityHeader from './components/Header'
import CitySearch from './components/Search'
import CityList from './components/list'
import SideNav from './components/Side-nav'
import Axios from 'axios'
export default {
    name: 'City',
    components: {
       CityHeader,
       CitySearch,
       CityList,
       SideNav
    },
   data () {
      return {
         Cityposition: [],
         cities: {},
         hotCities: [],
         letter: ''
      }
   }, 
   methods: {
      getInfoCity() {
         Axios.get('/api/city.json')
           .then(this.getSucessInfoCity)
      },
      getSucessInfoCity(res){
         res = res.data
         if(res.ret && res.data) {
            const data = res.data
             this.Cityposition = data.Cityposition
             this.cities = data.cities
             this.hotCities = data.hotCities
         }
      },
      handLetterChang (letter) {
          this.letter = letter
      }
   },
   mounted() {
      this.getInfoCity()
   },
}
</script>

<style>
</style>