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
.cd-card {
  background: #ffffff;
}

.cd-wrap {
  padding: 28px 34px;
}

.cd-title {
  color: #455a1f;
  font-size: 18px;
  margin-bottom: 14px;
  letter-spacing: 0.5px;
}

.cd-table :deep(th) {
  color: #455a1f;
  font-size: 12px;
  font-weight: 700;
  text-transform: uppercase;
  opacity: 0.9;
}

.cd-table :deep(td) {
  font-size: 14px;
  color: #455a1f;
}

.cd-name {
  color: #455a1f;
  font-weight: 600;
}

.cd-empty {
  padding: 18px 0;
  text-align: center;
  color: #455a1f;
  opacity: 0.8;
}

.cd-totalRow {
  margin-top: 14px;
  display: flex;
  justify-content: flex-end;
  gap: 14px;
  align-items: baseline;
  color: #455a1f;
}

.cd-totalLabel {
  color: #455a1f;
  font-weight: 700;
  text-transform: uppercase;
  font-size: 12px;
}

.cd-totalValue {
  color: #455a1f;
  font-weight: 800;
  font-size: 16px;
}

.cd-actions {
  margin-top: 18px;
  display: flex;
  justify-content: flex-end;
  gap: 12px;
}

.cd-pay,
.cd-continue {
  background: #d8d48a;
  color: #455a1f;
  font-weight: 800;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.12);
}

/* MOBITEL */
@media (max-width: 600px) {
  .cd-wrap {
    padding: 20px 15px;
  }

  .cd-table :deep(thead) {
    display: none;
  }

  .cd-table :deep(tr) {
    display: block;
    border-bottom: 2px solid #e9eef6;
    padding: 10px 0;
    position: relative;
  }

  .cd-table :deep(td) {
    display: flex;
    justify-content: space-between;
    align-items: center;
    border: none !important;
    padding: 4px 0 !important;
    text-align: right !important;
    font-size: 13px;
  }

  .cd-table :deep(td::before) {
    content: attr(data-label);
    font-weight: 700;
    font-size: 10px;
    text-transform: uppercase;
    color: #455a1f;
    opacity: 0.7;
  }

  .cd-name {
    font-size: 16px !important;
    color: #455a1f !important;
    margin-bottom: 4px;
  }

  .cd-table :deep(td:last-child) {
    position: absolute;
    top: 5px;
    right: -10px;
  }

  .cd-totalRow {
    justify-content: center;
    font-size: 18px;
    margin: 20px 0;
  }

  .cd-actions {
    flex-direction: column;
    width: 100%;
  }

  .cd-pay,
  .cd-continue {
    width: 100%;
  }
}
</style>
