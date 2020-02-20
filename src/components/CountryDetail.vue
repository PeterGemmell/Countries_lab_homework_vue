<template lang="html">
  <div v-if='country'>
    <br>
    <br>
    <h3 align="center"><u> {{ country.name }} </u></h3>
    <p>Capital: {{ country.capital }}</p>
    <p>Population: {{ country.population }}</p>
    <p>Region: {{ country.region }}</p>
    <br>
    <h4><u>Languages</u></h4>
    <p v-for="(language, index) in country.languages">{{language.name}}</p>
    <p>
    <img :src="country.flag">
  </p>
  </div>
</template>

<script>
export default {
  name: 'country-detail',
  props: ['country']
}
</script>

<style lang="css" scoped>
</style>
