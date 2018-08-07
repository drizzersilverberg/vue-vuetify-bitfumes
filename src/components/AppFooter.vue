<template lang="html">
  <v-footer height="auto">
    <v-card>
      <v-card-text class="teal white--text">
        <strong class="subheading text-md-center">Get connected with us on social networks!</strong>
        <v-spacer></v-spacer>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-3"
          dark
          icon
        >
          <v-icon size="24px">{{ icon }}</v-icon>
        </v-btn>
      </v-card-text>
      <v-card-text class="grey lighten-3">
        <v-layout>
          <v-flex
            v-for="(col, i) in rows"
            :key="i"
            xs3
          >
            <span class="body-2" v-text="col.title.toUpperCase()"></span>
            <div
              v-for="(child, i) in col.children"
              :key="i"
              v-text="child"
            />
          </v-flex>
          <v-flex xs3 layout column>
            <span class="body-2">CONTACT</span>
            <div>
              <v-icon size="18px" class="mr-3">fa-home</v-icon>
              New York, NY 10012, US
            </div>
            <div>
              <v-icon size="18px" class="mr-3">fa-envelope</v-icon>
              info@example.com
            </div>
            <div>
              <v-icon size="18px" class="mr-3">fa-phone</v-icon>
              + 01 234 567 89
            </div>
            <div>
              <v-icon size="18px" class="mr-3">fa-phone</v-icon>
              + 01 234 567 89
            </div>
          </v-flex>
        </v-layout>
      </v-card-text>
      <v-card-actions class="grey lighten-2 justify-center">
        &copy; 2018 - &nbsp;<strong>Vuetify</strong>
      </v-card-actions>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  data: () => ({
    icons: [
      'fa-facebook',
      'fa-twitter',
      'fa-google-plus',
      'fa-linkedin',
      'fa-instagram',
    ],
    rows: [
      {
        title: 'Company Name',
        children: ['Lorem ipsum dolor sit amet, consectetur adipisicing elit. Hic veritatis eligendi, accusamus molestias aut odit quas dignissimos porro aliquam deleniti incidunt, voluptatem ullam quasi officia veniam cumque, corporis quo minima.']
      },
      {
        title: 'Company Name',
        children: ['Lorem ipsum dolor sit amet, consectetur adipisicing elit. Hic veritatis eligendi, accusamus molestias aut odit quas dignissimos porro aliquam deleniti incidunt, voluptatem ullam quasi officia veniam cumque, corporis quo minima.']
      },
      {
        title: 'Company Name',
        children: ['Lorem ipsum dolor sit amet, consectetur adipisicing elit. Hic veritatis eligendi, accusamus molestias aut odit quas dignissimos porro aliquam deleniti incidunt, voluptatem ullam quasi officia veniam cumque, corporis quo minima.']
      },
    ]
  })
}
</script>

<style lang="css">
</style>
