<template>
    <v-container>
      <v-row>
        <v-col sm='12' md="6">
          <v-card>
            <v-card-title>{{ titleOne }}</v-card-title>
              <v-card-text>{{ serverActive }}</v-card-text>
              <v-btn @click="changeTitleOne()">Use this Server</v-btn>
          </v-card>
        </v-col>
        <v-col sm='12' md="6">
          <v-card>
            <v-card-title>{{ titleTwo }}</v-card-title>
            <v-card-text>{{ serverSuspended }}</v-card-text>
            <v-btn @click="changeTitleTwo()">Use this Server</v-btn>
          </v-card>
        </v-col>
          <v-col sm='12' md="6">
          <v-card>
            <v-card-title>Server 3</v-card-title>
            <v-card-text>{{ serverSuspended }}</v-card-text>
          </v-card>
        </v-col>
        <v-col sm='12' md="6">
          <v-card>
            <v-card-title>Server 4</v-card-title>
            <v-card-text>{{ serverActive }}</v-card-text>
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

    }),
    methods: {
        changeTitleOne() {
            bus.$emit('titleOneChanged', this.titleOne);
        },
        changeTitleTwo() {
            bus.$emit('titleTwoChanged', this.titleTwo);
        }
    }
}
</script>

<style scoped>

</style>