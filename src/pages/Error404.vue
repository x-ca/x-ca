<template>
  <q-page padding class="page-wrapper">
    <div class="text-center q-pa-md">
      <div style="font-size: 15vh">404</div>

      <div class="text-h5" style="opacity: 0.4">Oops. Nothing here...</div>

      <q-btn class="q-mt-xl" unelevated to="/" label="Go Home" no-caps />
    </div>
  </q-page>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Error404',
});
</script>
