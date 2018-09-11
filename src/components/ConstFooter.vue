<template>
  <v-footer :fixed="fixed" app color="secondary">
    <v-spacer/>
    <span>&copy; 2017</span>
    <v-spacer/>
  </v-footer>
</template>


<script>
export default {
  name: 'ConstFooter',
  data () {
    return {
      fixed: true
    }
  }
}
</script>


<style scoped>
</style>