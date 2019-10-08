<template>
    <v-container>
        <v-row>
            <v-col>
                <v-card>
                    <v-card-title>{{ title }}</v-card-title>
                    <v-card-text> {{ status }} </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import { bus } from '../main';
export default {
    data: () => ({
        title: 'Select Server',
        status: 'Unavailable'
    }),
    created() {
        bus.$on('titleOneChanged', (data, server) => {
            this.title = data;
            this.status = server;
        });

        bus.$on('titleTwoChanged', (data, server) => {
            this.title = data;
            this.status = server;
        });

        bus.$on('titleThreeChanged', (data, server) => {
            this.title = data;
            this.status = server;
        });
        bus.$on('titleFourChanged', (data, server) => {
            this.title = data;
            this.status = server;
        });
    }
    
}
</script>


<style scoped>

</style>