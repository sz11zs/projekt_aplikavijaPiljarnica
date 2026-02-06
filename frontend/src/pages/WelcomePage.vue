<template>
  <div class="welcome-page">
    <v-container fluid class="welcome-container">
      <!-- Slika + naslov gore -->
      <div class="top">
        <v-img :src="pocetnaSlika" max-width="520" class="mx-auto" contain />
        <div class="brand-title mt-2">Piljarnica NOVA</div>
      </div>

      <!-- Zeleni panel -->
      <v-card class="panel" rounded="xl" elevation="0">
        <div class="panel-text">
          Drago nam je što koristite našu aplikaciju za kupnju. Za obavljanje kupnje potrebno je imati korisnički račun. Ako želite prvo istražiti ponudu, možete nastaviti kao gost.
          <br /><br />
          Uživajte u kupnji !!
        </div>

        <div class="panel-actions">
          <v-btn class="btn-guest" rounded="pill" variant="outlined" to="/trgovina">
            GOST
          </v-btn>
          <v-btn class="btn-register" rounded="pill" to="/registracija">
            REGISTRIRAJ SE
          </v-btn>
        </div>
      </v-card>
    </v-container>
  </div>
</template>

<script setup lang="ts">
  import pocetnaSlika from '@/assets/pocetnaSlika.png'
</script>

<style scoped>
.welcome-page {
  height: 100vh; /* Fiksna visina ekrana */
  overflow: hidden; /* Sprječava pojavu scrollbara */
  display: flex;
  align-items: center;
  justify-content: center;
  background: #ffffff;
}

.welcome-container {
  padding-top: 0;
  padding-bottom: 0;
}

.top {
  text-align: center;
  margin-bottom: 40px;
}

.brand-title {
  font-family: "Architects Daughter", cursive;
  color: #455a1f;
  font-size: 72px;
  line-height: 1;
  margin-top: 8px;
}

/* ZELENI PANEL – FIGMA */

.panel {
  background: #455a1f;
  padding: 56px 72px;
  border-radius: 48px;
  width:100%;
}

.panel-text {
  color: #ffffff;
  font-size: 24px;
  line-height: 1.5;
}

.panel-actions {
  margin-top: 48px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

/* GUMBI */

.btn-guest {
  border-color: #ffffff;
  color: #ffffff;
  min-width: 300px;
  height: 56px;
  font-size: 18px;
}

.btn-register {
  background: #d8d48a;
  color: #455a1f;
  font-weight: 600;
  min-width: 300px;
  height: 56px;
  font-size: 18px;
}

/* RESPONSIVE – TABLET */

@media (max-width: 960px) {

  .brand-title {
    font-size: 52px;
  }

  .panel {
    padding: 36px 32px;
    border-radius: 32px;
  }

  .panel-text {
    font-size: 20px;
  }
}

/* RESPONSIVE – MOBITEL */

@media (max-width: 600px) {
  .welcome-container {
  padding-top: 32px;
  padding-bottom: 48px;
  }

  .brand-title {
    font-size: 40px;
  }

  .panel {
    padding: 24px 20px;
    border-radius: 24px;
  }

  .panel-text {
    font-size: 18px;
  }

  .panel-actions {
    flex-direction: column;
    gap: 16px;
    margin-top: 32px;
  }

  .btn-register {
    width: 100%;
    min-width: unset;
  }
}
</style>
