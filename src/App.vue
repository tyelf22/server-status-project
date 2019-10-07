<template>
  <v-app>
    <header></header>

  <v-content>
   <v-container>
     <v-row>
       <v-col md="9">
          <all-servers></all-servers>
        </v-col>
        <v-col md='3'>
          <h1>Hello</h1>
        </v-col>
      </v-row>
    </v-container>
  </v-content>

  </v-app>
</template>

<script>
import AllServers from './components/allServers'
import Header from './components/header'


export default {
  name: 'App',
  components: {
    AllServers,
    Header
  },
  data: () => ({
    //
  }),
};
</script>
