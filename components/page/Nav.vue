<template>
    <div>
        <v-navigation-drawer fixed v-model="drawer" app>
            <v-list dense>
                <v-list-tile>
                    <v-list-tile-action>
                        <v-icon>home</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <nuxt-link to="/"><v-list-tile-title>Dashboard</v-list-tile-title></nuxt-link>
                    </v-list-tile-content>
                </v-list-tile>

                <v-list-tile>
                    <v-list-tile-action>
                        <v-icon>edit</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <nuxt-link to="/tools/posts"><v-list-tile-title>Posts</v-list-tile-title></nuxt-link>
                    </v-list-tile-content>
                </v-list-tile>
                
                <v-list-tile>
                    <v-list-tile-action>
                        <v-icon>subject</v-icon>
                    </v-list-tile-action>
                    <v-list-tile-content>
                        <nuxt-link to="/tools/sections"><v-list-tile-title>Sections</v-list-tile-title></nuxt-link>
                    </v-list-tile-content>
                </v-list-tile>
            </v-list>
        </v-navigation-drawer>

        <v-toolbar dark fixed app>
            <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
            <v-toolbar-title>Blog Kernel CMS</v-toolbar-title>
        </v-toolbar>
    </div>
</template>

<script>
import jav from '~/components/page/Nav.vue'

export default {
   data () {
      return {
        drawer : false
      }
   }
}
</script>