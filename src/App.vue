<template>
  <v-app>
    <div id="nav">
      <v-navigation-drawer
        v-model="sideNav"
        app
        >
        <v-list>
          <v-list-tile>
            <v-list-tile-action>
              <v-icon>home</v-icon>
            </v-list-tile-action>
              <v-list-tile-content><router-link to="/">Home</router-link></v-list-tile-content>
          </v-list-tile>
          <v-list-tile>
            <v-list-tile-action>
              <v-icon>trending_up</v-icon>
            </v-list-tile-action>
              <v-list-tile-content><router-link to="/about">About</router-link></v-list-tile-content>
          </v-list-tile>
        </v-list>
      </v-navigation-drawer>
      <v-toolbar app 
        scroll-off-screen 
        scroll-threshold:50
        >
        <v-toolbar-side-icon
          @click.stop="sideNav = !sideNav"
          >
        </v-toolbar-side-icon>
        <v-spacer></v-spacer>
        <v-toolbar-items>
          <v-btn flat @click="profile">
            <v-icon left>supervisor_account</v-icon>
            Profil
          </v-btn>
        </v-toolbar-items>
      </v-toolbar>
    </div>
    <v-content app>
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>
  export default {
    data () {
      return {
        sideNav: false
      }
    },
    methods: {
      profile () {
        this.$router.push('login')
      }
    }
  }

</script>
