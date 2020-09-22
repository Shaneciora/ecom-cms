<template>
    <div class="start">
        
        <div id="header">

        </div>

        <div id="content">
            <v-container fill-height fluid>
                <v-row>
                    <v-col>
                        <v-app>
                        <router-link to="Creator" text-decoration="none">
                        <v-btn class="ma-2" outlined color="blue">Create a New Site</v-btn>
                        </router-link>
                        </v-app>
                    </v-col>
                </v-row>
            </v-container>
        </div>
    </div>
</template>

<style>
    #content {
        font-family: Avenir, Helvetica, Arial, sans-serif;
        text-align: center;
        padding-top: 35%;
    }

    a {
        text-decoration: none;
    }
</style>

<script>
    export default {
        methods: {
            start_run: function() {
               
            }
        },
    }
</script>
