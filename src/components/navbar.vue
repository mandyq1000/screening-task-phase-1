<template>
      <v-app>
        <v-app-bar
          app
          color="indigo"
          dark
        >
          <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>
          <v-toolbar-title>Application</v-toolbar-title>
        </v-app-bar> 

        <v-navigation-drawer
          v-model="drawer"
          app
        >
          <v-list nav dense>
             <v-list-item-group
          v-model="group"
          active-class="indigo--text text--accent-4"
        >
            <v-list-item v-for="link in links" :key="link.text" router :to="link.path">
             
                <v-icon>{{link.icon}}</v-icon>
             
                <v-list-item-title>{{link.text }}</v-list-item-title>
              
            </v-list-item>
             </v-list-item-group>
          </v-list>
        </v-navigation-drawer>
      
      
       <v-footer
          color="indigo"
          app
        >
          <span class="white--text">&copy; {{ new Date().getFullYear() }}</span>
        </v-footer>
      
      </v-app>
</template>

<script>
export default {
     data: () => ({
     drawer: false,
     links: [
     { icon: 'mdi-home', text: 'Home', path:'/' },
     { icon: 'mdi-car', text: 'About', path:'/about' },
     ]
      })
    
}
</script>