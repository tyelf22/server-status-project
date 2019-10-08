<template>
  <v-app>
    <!-- Navigation -->
    <nav>
      <top-header></top-header>
    </nav>
    <!-- Main Content -->
  <v-content>
   <v-container>
     <v-row>
       <v-col md="9">
          <all-servers></all-servers>
        </v-col>
        <v-col md='3'>
          <server-details></server-details>
        </v-col>
      </v-row>
    </v-container>
  </v-content>

  </v-app>
</template>

<script>
import AllServers from './components/allServers'
import TopHeader from './components/header'
import ServerDetails from './components/serverDetails'


export default {
  name: 'App',
  components: {
    AllServers,
    TopHeader,
    ServerDetails
  },
  data: () => ({
    //
  }),
};
</script>
