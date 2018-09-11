<template>
  <v-container>
    <v-tabs
      slider-color="blue"
      fixed-tabs
    >
      <v-tab>Kaydol</v-tab>
      <v-tab>Giris Yap</v-tab>
      <v-tab-item>
        <h1>TOO SEXY EH?</h1>
      </v-tab-item>
      <v-tab-item>
        <v-form>
          <v-text-field
            v-model="email"
            :rules="emailRules"
            label="E-Mail"
            required
          ></v-text-field>
          <v-text-field
            v-model="password"
            label="Password"
            required
          ></v-text-field>
        </v-form>
      </v-tab-item>
    </v-tabs>
  </v-container>
</template>



<script>
export default {
  name: 'Authenticate',
// #DEVAM
  data () {
  }
}
</script>


