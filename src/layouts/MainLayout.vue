<template>
  <q-layout class="bg-grey-1">
    <Header />

    <q-page-container>
      <router-view />
    </q-page-container>

    <Footer />
  </q-layout>
</template>

<script>
import Header from 'src/components/layout/Header.vue';
import Footer from 'src/components/layout/Footer.vue';

export default {
  name: 'MainLayout',
  components: {
    Header,
    Footer,
  },
};
</script>
