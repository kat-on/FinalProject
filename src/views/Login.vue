<template>
<div class=" container">
  <v-card :loading="loading" class="mx-auto my-12" max-width="374">
    <v-subheader height="200">
      <h1>Login</h1>
    </v-subheader>
    <v-card-text>
      <v-row align="center" class="mx-0">
        <v-text-field
          v-model="input.username"
          :type="'text' "
          :prepend-icon="'mdi-account'"
          name="input-10-1"
          label="username"
        ></v-text-field>
        <v-text-field
          v-model="input.password"
          :type="'password'"
          :prepend-icon="'mdi-key-variant'"
          name="input-10-1"
          label="password"
          hint="At least 8 characters"
        ></v-text-field>
      </v-row>
    </v-card-text>
    <v-divider class="mx-4"></v-divider>
    <v-card-actions>
      <v-btn color="deep-purple accent-4" text @click="reserve()">Login</v-btn>
    </v-card-actions>
  </v-card>
</div>
</template>
<script>
export default {
  data: () => ({
    loading: false,
    selection: 1,
    input: {
        username: '',
        password: '' 
      },
  }),

  methods: {
    reserve() {
      this.loading = true;
       this.$router.push("/reserved");
      setTimeout(() => (this.loading = false), 5000);
      if(username==="" && password===""){
        alert("field is required");
      }else{

      }
    }
  }
};
</script>
<style scoped>
.container{
  border:2px solid grey;
  margin-top:5%;
  width:70%;
  background-image: url("https://images.fineartamerica.com/images/artworkimages/mediumlarge/1/chattanooga-riverwalk-night-black-and-white-larry-underwood.jpg")
}
.theme--light.v-subheader {
  background-color: #1976d2;
  height: 100px;
}
.btn {
  margin-left: 30px;
}
.v-card__actions .v-btn.v-btn {
  padding: 0 8px;
  background-color: #1976d2;
  margin-left: 109px;
  width: 135px;
}

</style>
