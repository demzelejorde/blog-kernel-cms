<template>
  <div>
    <v-app>
      <v-nav></v-nav>
      <v-content>
        <v-container fluid fill-height>
          <v-layout>
            <nuxt/>
          </v-layout>
        </v-container>
      </v-content>
    </v-app>
  </div>
</template>

<script>
import vNav from '~/components/page/Nav.vue'

export default {
  components: {
    vNav
  }
}
</script>
