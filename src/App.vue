<template>
  <v-app>
    <!-- Navigation -->
    <nav>
      <top-header></top-header>
    </nav>
    <!-- Main Content -->
  <v-content>
      <server-details></server-details>
      <all-servers></all-servers>
 
  </v-content>
     <bottom-footer></bottom-footer>
  </v-app>
</template>

<script>
import AllServers from './components/allServers'
import TopHeader from './components/header'
import ServerDetails from './components/serverDetails'
import BottomFooter from './components/footer'


export default {
  name: 'App',
  components: {
    AllServers,
    TopHeader,
    ServerDetails,
    BottomFooter
  },
  data: () => ({
    //
  }),
};
</script>
