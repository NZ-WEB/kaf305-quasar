<template>
  <q-layout view="hHh Lpr lff">
    <q-header>
      <q-toolbar>
        <q-btn flat round dense icon="menu" class="q-mr-sm" />

        <q-space />

        <q-btn-toggle
          v-model="model"
          flat
          stretch
          toggle-color="yellow"
          :options="options"
        />
      </q-toolbar>
    </q-header>

    <!-- <the-drawer :isleftDrawerOpen="isleftDrawerOpen" /> -->

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent, ref } from 'vue';
import TheDrawer from 'src/components/TheDrawer.vue';

export default defineComponent({
  name: 'MainLayout',
  setup() {
    // const isleftDrawerOpen = ref(false);
    const model = ref('one');

    const toggleLeftDrawer = () => {
      // isleftDrawerOpen.value = !isleftDrawerOpen.value;
    };

    return {
      model,
      // isleftDrawerOpen,
      toggleLeftDrawer,
      options: [
        { label: 'One', value: 'one' },
        { label: 'Two', value: 'two' },
        { label: 'Three', value: 'three' },
      ],
    };
  },
  // components: { TheDrawer },
});
</script>
