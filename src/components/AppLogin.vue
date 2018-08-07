<template lang="html">
  <v-container>
    <v-alert type="warning" color="lime" :value="alert">
      Please fill email and password
    </v-alert>
    <v-form @submit.prevent="submit">
      <v-text-field
        label="E-mail"
        v-model="email"
        required
      ></v-text-field>
      <v-text-field
        label="Password"
        v-model="password"
        type="password"
        required
      ></v-text-field>
      <v-btn color="green" type="submit">Login</v-btn>
    </v-form>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      email: null,
      password: null,
      alert: false,
    }
  },
  methods: {
    submit() {
      if (!this.email && !this.password) {
        this.alert = true
      }
      console.log(`Email is ${this.email} and Password is ${this.password}`)
    }
  }
}
</script>

<style lang="css">
</style>
