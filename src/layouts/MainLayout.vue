<template>
  <q-layout view="hHh Lpr lff">
    <q-header>
      <q-toolbar>
        <q-btn
          aria-label="Menu"
          dense
          flat
          icon="menu"
          round
          @click="toggleLeftDrawer"
        />

      <q-toolbar-title> Quasar App</q-toolbar-title>

      <q-btn
        aria-label="dark mode"
        dense
        flat
        icon="settings"
        round
        @click="toggleDarkMode"
      />

        <div>Quasar v{{ $q.version }}</div>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="isLeftDrawerOpen" show-if-above>
      <the-drawer :is-left-drawer-open="isLeftDrawerOpen"/>
    </q-drawer>

    <q-page-container>
      <router-view/>
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import {defineComponent, ref} from 'vue';
import {useQuasar} from 'quasar';

import TheDrawer from 'src/components/TheDrawer.vue';

export default defineComponent({
  name: 'MainLayout',
  setup() {
    const isLeftDrawerOpen = ref(false);
    const $q = useQuasar()

    const toggleLeftDrawer = () => {
      isLeftDrawerOpen.value = !isLeftDrawerOpen.value;
    };

    const toggleDarkMode = () => {
      console.log(console.log($q.dark.isActive))
      $q.dark.toggle()
    };

    return {
      isLeftDrawerOpen,
      toggleLeftDrawer,
      toggleDarkMode,
    };
  },
  components: {TheDrawer},
});
</script>
