<template>
  
  <v-app>
    <v-card height="100%">
       <div ref="container"> 
            <!--<button @click="onClick">Click to insert</button>-->
        </div>

    </v-card>
  </v-app>

</template>

<script>
/* eslint-disable vue/no-unused-components */
import Vue from 'vue'
import Menu from './creator_components/creator_Menu.vue'

	export default {
    name: 'app',
    components: { Menu },
    methods: {
      addMenu() {
        var ComponentClass = Vue.extend(Menu)
        var instance = new ComponentClass({
            propsData: { type: 'primary' }
        })
        instance.$mount() // pass nothing
//         console.log(this.$refs)
        this.$refs.container.appendChild(instance.$el)
      }
    },
    created() {
    // set componenent name
        this.$root.$refs.creator_content = this;
    }
  }
</script>
<style>
</style>