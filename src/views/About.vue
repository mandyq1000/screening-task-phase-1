<template>
          <v-app>
          <v-container class="fill-height blue lighten-5" fluid transition="slide-x-transition">   
              <v-row class="justify-center">
                  <v-col cols="8">
                    <v-card
                    class="mx-auto"
                    max-width="1000"
                    tile
                  >
                  <v-list-group
                  prepend-icon="mdi-account-box"
                  value="true"
                  >
                  <template v-slot:activator>
                    <v-list-item-title>Users</v-list-item-title>
                  </template>
                  <v-list-item
                  v-for="(crud, i) in cruds"
                  :key="i"
                  click=""
                >
                  <v-list-item-title v-text="crud[0]"></v-list-item-title>
                  <v-list-item-action>
                    <v-icon v-text="crud[1]"></v-icon>
                  </v-list-item-action>
                </v-list-item>
                </v-list-group>                  
                    </v-card>
                  
                </v-col>
                
              </v-row>        
              
          </v-container>
        </v-app> 
</template>


 <script>
 

    export default {
      data: () => ({
        drawer: false,
        cruds: [
            ['Create', 'mdi-car'],
            ['Read', 'mdi-car'],
            ['Update', 'mdi-update'],
            ['Delete', 'mdi-delete'],
          ],
      })
    }  
</script>
