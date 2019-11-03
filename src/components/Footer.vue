<template>
  <v-footer padless>
    <v-col class="text-center caption" cols="12">
      {{ new Date().getFullYear() }} —
      <strong>
        A project by Baffour Adu Boampong. Code &amp; design licensed under MIT.
      </strong>
    </v-col>
  </v-footer>
</template>

<script lang="ts">
import { Vue, Component } from "vue-property-decorator";

@Component
export default class Footer extends Vue {}
</script>
