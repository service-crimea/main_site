<template>
  <div>
    <h3>{{ textSearch }} (length: {{ textSearch.length }}) </h3>
    <input type="text" size="50" v-model="textSearch">
    <button type="button" @click="getSearch">грузи</button>
  </div>
</template>

<script type="text/javascript">
export default {
  name: 'search_component',
  data() {
    return {
      textSearch: ''
    }
  },
  watch: {
    textSearch: function() {
      if ( this.textSearch.length > 3 ) {
        this.textSearch = 'chenge text on the field'
      }
    }
  },
  methods: {
    getSearch() {
      console.log("")
    }
  }
}
</script>

<style scoped>
</style>