<template>
    <v-container>
      <v-row>
        <v-col>
          <v-card>
            <v-card-title>{{ titleOne }} <v-icon>mdi-database-check</v-icon> </v-card-title>
              <v-card-text>{{ serverActive }}</v-card-text>
              <v-btn ripple width="100%" color='primary' @click="changeTitleOne()">Use this Server</v-btn>
          </v-card>
        </v-col>
        <v-col >
          <v-card>
            <v-card-title>{{ titleTwo }} <v-icon>mdi-database-remove</v-icon> </v-card-title>
            <v-card-text>{{ serverSuspended }}</v-card-text>
            <v-btn ripple width="100%" color='primary' @click="changeTitleTwo()">Use this Server</v-btn>
          </v-card>
        </v-col>
       </v-row>
       <v-row>
          <v-col>
          <v-card>
            <v-card-title>{{titleThree}} <v-icon>mdi-database-remove</v-icon> </v-card-title>
            <v-card-text>{{ serverSuspended }}</v-card-text>
            <v-btn ripple width="100%" color='primary' @click="changeTitleThree()">Use this Server</v-btn>
          </v-card>
        </v-col>
        <v-col>
          <v-card>
            <v-card-title>{{titleFour}}<v-icon>mdi-database-check</v-icon> </v-card-title>
            <v-card-text>{{ serverActive }}</v-card-text>
            <v-btn ripple width="100%" color='primary' @click="changeTitleFour()">Use this Server</v-btn>
          </v-card>
        </v-col>
      </v-row>
    </v-container> 
</template>

<script>
import { bus } from '../main';

export default {
    data: () => ({
        serverActive: 'Active',
        serverSuspended: 'Suspended',
        titleOne: 'Server One',
        titleTwo: 'Server Two',
        titleThree: 'Server Three',
        titleFour: 'Server Four'
    }),

    icons: [
        'mdi-database-check',
        'mdi-database-remove'
    ],
    methods: {
        changeTitleOne() {
            bus.$emit('titleOneChanged', this.titleOne, this.serverActive);
        },
        changeTitleTwo() {
            bus.$emit('titleTwoChanged', this.titleTwo, this.serverSuspended);
        },
        changeTitleThree() {
            bus.$emit('titleTwoChanged', this.titleThree, this.serverSuspended);
        },
        changeTitleFour() {
            bus.$emit('titleTwoChanged', this.titleFour, this.serverActive);
        }
    }
}
</script>

<style scoped>


</style>