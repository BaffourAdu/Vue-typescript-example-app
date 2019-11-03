<template>
  <v-footer padless>
    <v-col class="text-center caption" cols="12">
      {{ new Date().getFullYear() }} —
      <strong>
        A project by Baffour Adu Boampong. Code &amp; design licensed under MIT.
      </strong>
      <br />
      <a href="https://github.com/BaffourAdu/Vue-typescript-example-app">
        View Project on Github
      </a>
    </v-col>
  </v-footer>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class Footer extends Vue {}
</script>
