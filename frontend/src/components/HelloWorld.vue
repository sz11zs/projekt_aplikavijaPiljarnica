<template>
  <v-app id="inspire">
    <v-navigation-drawer v-model="drawer" app>
      <v-list class="d-flex flex-column fill-height" nav>
        <!-- GORNJE STAVKE -->
        <div class="pt-16">
          <v-list-item
            title="O aplikaciji"
            prepend-icon="mdi-information-outline"
            to="/about"
          />
          <v-list-item
            title="Registracija/Prijava"
            prepend-icon="mdi-storefront-outline"
            to="/registracija"
          />
          <v-list-item
            title="Trgovina"
            prepend-icon="mdi-storefront-outline"
            to="/trgovina"
          />
        </div>

        <!-- GURA SVE PREMA GORE -->
        <v-spacer />

        <!-- DONJA STAVKA -->
        <v-divider />
        <v-list-item
          title="Dashboard"
          prepend-icon="mdi-view-dashboard-outline"
          to="/dashboard"
        />
      </v-list>
    </v-navigation-drawer>

    <v-app-bar>
      <v-app-bar-nav-icon color="#455A1F" @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-app-bar-title>
        <span class="navbar-title">Piljarnica NOVA</span>
      </v-app-bar-title>

      <v-btn flat color="grey">
        <span>Sing Out</span>
        <v-icon end>exit_to_app</v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <v-container class="d-flex justify-center pt-16">
        <v-img :src="pocetnaSlika" max-width="640" contain />
      </v-container>
      <div class="piljarnica-title mt-n1">Piljarnica NOVA</div>
    </v-main>
  </v-app>
</template>

<script setup>
  import { ref } from "vue";
  import pocetnaSlika from "@/assets/pocetnaSlika.png";

  const drawer = ref(null);

  export default {
data: () => ({ drawer: null }),
 };
</script>

<style scoped>
.piljarnica-title {
  font-family: "Architects Daughter", cursive;
  color: #455a1f;
  line-height: 1;
  text-align: center;

  font-size: 40px; /* mobitel */
}

@media (min-width: 600px) {
  .piljarnica-title {
    font-size: 64px; /* tablet */
  }
}

@media (min-width: 1264px) {
  .piljarnica-title {
    font-size: 96px; /* desktop – Figma */
  }
}
.navbar-title {
  font-family: 'Architects Daughter', cursive;
  color: #455A1F;
  font-size: 14px; /* mobitel */
  line-height: 1;
}

@media (min-width: 600px) {
  .navbar-title {
    font-size: 16px; /* tablet */
  }
}

@media (min-width: 1264px) {
  .navbar-title {
    font-size: 18px; /* desktop */
  }
}

</style>
