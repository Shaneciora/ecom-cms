<template>
    <v-app>
        <v-card
            height="100%"
            width="256"
            flat
            
        >
            <v-navigation-drawer floating permanent>
            <v-list-item>
                <v-list-item-content>
                <v-list-item-title class="title">
                    <center>Add Elements</center>
                </v-list-item-title>
                </v-list-item-content>
            </v-list-item>

            <v-divider></v-divider>

            <v-list
                dense
                rounded
                nav
            >
                <v-list-item
                v-for="item in add_elements"
                :key="item.title"
                link
                @click="addElement(item.function)"
                >
                <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
                </v-list-item>
            </v-list>

            <v-divider></v-divider>
            <v-list-item>
                <v-list-item-content>
                <v-list-item-title class="title">
                    <center>Current Elements</center>
                </v-list-item-title>
                </v-list-item-content>
            </v-list-item>

            <v-list
                dense
                rounded
                nav
            >
                <v-list-item
                v-for="item in current_elements"
                :key="item.title"
                link
                
                >
                <v-list-item-icon>
                    <v-icon>{{ item.icon }}</v-icon>
                </v-list-item-icon>

                <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                </v-list-item-content>
                </v-list-item>
            </v-list>

            </v-navigation-drawer>
        </v-card>
    </v-app>
</template>

<style scoped>
    *{
        font-family: Avenir, Helvetica, Arial, sans-serif;
    }
        
</style>
<script>
import '@mdi/font/css/materialdesignicons.css'
  export default {
      

    data () {
      return {
        add_elements: [
          { title: 'Menu', icon: 'menu', function: 'Menu'},
          { title: 'Title', icon: 'title', function: 'Title'},
          { title: 'TextBox', icon: 'question_answer', function: 'TextBox' },
        ],
        current_elements: [],
        right: null,
      }
    },

    methods: {
        addElement(element){
            if(element == "Menu"){
                this.current_elements.push({  title: 'c_Menu', icon:"delete"})
                this.$root.$refs.creator_content.addMenu();
            }else if(element == "Title"){
                this.current_elements.push({  title: 'c_Title', icon:"delete"})
                //this.$root.$refs.creator_content.addTitle();
            }else if(element == "TextBox"){
                this.current_elements.push({  title: 'c_TextBox', icon:"delete"})
                //this.$root.$refs.creator_content.addTextBox();
            }
        },
    }
  }
</script>