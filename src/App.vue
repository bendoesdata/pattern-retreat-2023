<template>
  <v-app>
    <v-main>
      <v-container>
        <h1>Pattern: See and Understand Data</h1>
        <v-expansion-panels>
          <v-expansion-panel>
            <v-expansion-panel-title> MINERVA </v-expansion-panel-title>
            <v-expansion-panel-text>
              <h2>formatted text</h2>
              <p>paragraph text</p>
            </v-expansion-panel-text>
          </v-expansion-panel>
          <v-expansion-panel>
            <v-expansion-panel-title> GutSee </v-expansion-panel-title>
            <v-expansion-panel-text>
              <h2>formatted text</h2>
              <p>paragraph text</p>
            </v-expansion-panel-text>
          </v-expansion-panel>
          <v-expansion-panel>
            <v-expansion-panel-title> Polygenic Risk Scores Explained </v-expansion-panel-title>
            <v-expansion-panel-text>
              <h2>formatted text</h2>
              <p>paragraph text</p>
            </v-expansion-panel-text>
          </v-expansion-panel>
        </v-expansion-panels>
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    trip: {
      name: "",
      location: null,
      start: null,
      end: null,
    },
    locations: [
      "Australia",
      "Barbados",
      "Chile",
      "Denmark",
      "Ecuador",
      "France",
    ],
  }),
};
</script>
