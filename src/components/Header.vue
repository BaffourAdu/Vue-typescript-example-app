<template>
  <div>
    <v-toolbar max-height="64">
      <v-toolbar-title>Conduit</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn text>Home</v-btn>
        <v-btn text>New Post</v-btn>
        <v-btn text>Settings</v-btn>
        <v-btn text>Sign up</v-btn>
      </v-toolbar-items>

      <v-app-bar-nav-icon
        class="hidden-md-and-up"
        @click.stop="drawer = !drawer"
      ></v-app-bar-nav-icon>
    </v-toolbar>

    <v-navigation-drawer v-model="drawer" absolute temporary>
      <v-list dense>
        <v-list-item
          v-for="item in drawerNavigationItems"
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
  </div>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class Header extends Vue {
  drawer: boolean = false;
  drawerNavigationItems: any[] = [
    { title: "Home", icon: "mdi-home-outline" },
    { title: "New Post", icon: "mdi-newspaper-plus" },
    { title: "Settings", icon: "mdi-tune" },
    { title: "Sign Up", icon: "mdi-account-plus-outline" }
  ];
}
</script>
