<template>
    <v-container>
        <v-row>
            <v-col>
                <v-card>
                    <v-card-title>{{ title }}</v-card-title>
                    <v-card-text> {{}} </v-card-text>
                </v-card>
            </v-col>
        </v-row>
    </v-container>
</template>

<script>
import { bus } from '../main';
export default {
    data: () => ({
        title: 'Server Details',
    }),
    created() {
        bus.$on('titleOneChanged', (data) => {
            this.title = data;
        });

        bus.$on('titleTwoChanged', (data) => {
            this.title = data;
        });
    }
    
}
</script>


<style scoped>

</style>