<template>
  <app-card class="q-ma-md">
    <q-card-section>
      <div class="text-h6">Меню</div>
      <div class="text-subtitle2">Кафедра 305</div>

      <q-list>
        <q-item clickable v-ripple>
          <q-item-section>Single line item</q-item-section>
        </q-item>

        <q-item clickable v-ripple>
          <q-item-section>
            <q-item-label>Item with caption</q-item-label>
            <q-item-label caption>Caption</q-item-label>
          </q-item-section>
        </q-item>

        <q-item clickable v-ripple>
          <q-item-section>
            <q-item-label overline>OVERLINE</q-item-label>
            <q-item-label>Item with caption</q-item-label>
          </q-item-section>
        </q-item>

        <q-item clickable v-ripple>
          <q-item-section>
            <q-item-label overline>OVERLINE</q-item-label>
            <q-item-label>Item with caption</q-item-label>
          </q-item-section>
        </q-item>
      </q-list>
    </q-card-section>

    <q-card-actions>
      <q-space />

      <q-btn
        color="grey"
        round
        flat
        dense
        :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
        @click="expanded = !expanded"
      />
    </q-card-actions>

    <q-slide-transition>
      <div v-show="expanded">
        <q-separator />
        <q-card-section class="text-subitle2">
          {{ lorem }}
        </q-card-section>
      </div>
    </q-slide-transition>
  </app-card>
</template>

<script lang="ts">
import { ref } from 'vue';
import AppCard from 'components/AppCard.vue';

export default {
  components: { AppCard },
  props: {
    isLeftDrawerOpen: {
      type: Boolean,
      default: false,
    },
  },

  // name: 'ComponentName',
  setup() {
    const expanded = ref(false);
    const tabs = ref('mail');

    return {
      expanded,
      tabs,
      lorem:
        'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Unde reiciendis magnam iure enim sit itaque illum distinctio porro laborum, tempore dolorum voluptas eaque eos. Mollitia nulla dolorem illo cumque quibusdam.',
    };
  },
};
</script>
