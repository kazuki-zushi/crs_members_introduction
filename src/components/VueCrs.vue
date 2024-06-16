<template>
  <v-app id="inspire">
    <v-app-bar extended>
            <!-- 反映されていない -->
      <v-img src="/vue-crs/img/logo_levtech.png" height="40" alt="Levtech Logo">Levtech</v-img>
      <v-spacer></v-spacer>

      <v-btn icon="mdi-dots-vertical">
      </v-btn>
    </v-app-bar>

    <v-main class="background">
      <v-container>
        <v-row>
          <v-col
            v-for="person in team"
            :key="person.avatar"
            cols="3"
            class="profile-col"
          >
            <v-card class="profile-card">
              <v-responsive ratio="4/3">
                <v-img :src="person.avatar" alt="Profile Image" class="profile-img"></v-img>
              </v-responsive>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
    <v-footer>
    </v-footer>
  </v-app>
</template>


<script>
  export default {
    data() {
      return { 
        team: [
        { avatar:"/vue-crs/img/avatar-1.png"},
        { avatar:"/vue-crs/img/avatar-2.png"},
        { avatar:"/vue-crs/img/avatar-3.png"},
        { avatar:"/vue-crs/img/avatar-4.png"}
        ]
       
      }
    }
  }
</script>


<style>
.profile-card {
  width: 259px;
  height: 337px;
  /* 反映されていない */
  border-radius: 30px;
  background-color: rgba(235, 123, 167, 0.5);
  overflow: hidden;
  /* Ensure the image fills the card */
  display: flex;
  align-items: center;
  justify-content: center;
}

.profile-img {
  width: 100%;
  height: 100%;
  object-fit: cover;  
}

.profile-col {
  margin-bottom: 40px;
}

.background{
background-color: #FFFAEB;
}

</style>