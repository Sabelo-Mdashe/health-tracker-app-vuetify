<template>
  <v-container>
    <v-navigation-drawer
      v-model="drawer"
      permanent
      app
      dark
      mini-variant
      mini-variant-width="100"
      class="pt-4 teal"
    >
      <v-list>
        <v-list-item class="mb-12">
          <v-list-item-content>
            <v-icon class="mb-2" large>
              fa-solid fa-hand-holding-medical
            </v-icon>
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <v-list flat>
        <v-list-item
          v-for="item in items"
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
      <v-list style="position: absolute; bottom: 0" class="ml-3" flat>
        <v-list-item>
          <v-list-item-icon>
            <v-icon right>mdi-logout</v-icon>
          </v-list-item-icon>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-container>
</template>

<script>
  export default {
    data() {
        return {
            drawer: true,
            items: [
                { title: "Home", icon: "mdi-home", to: "/" },
                { title: "My Account", icon: "mdi-account" },
                { title: "Users", icon: "mdi-heart" },
                { title: "Users", icon: "mdi-email" },
                { title: "Users", icon: "mdi-cog" },
                { title: "Users", icon: "mdi-help-circle" },
            ],
            mini: true,
        };
    },
  }
</script>
