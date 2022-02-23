<template>
  <q-page>
    <div class="row q-pa-md q-gutter-lg">
      <div class="col-8">
        <app-card>
          <q-card-section>
            <q-btn
              fab
              color="primary"
              icon="place"
              class="absolute"
              style="top: 0; right: 12px; transform: translateY(-50%)"
            />

            Lorem ipsum dolor sit amet consectetur adipisicing elit. Placeat
            iusto optio minima repellendus delectus id accusamus non voluptate!
            Eius esse aliquid delectus aspernatur? Lorem, ipsum. Lorem ipsum,
            dolor sit amet consectetur adipisicing elit. Neque quaerat est at
            tempore minima temporibus! Ad unde ut et, natus molestias expedita
            rem id nulla quia eligendi hic quasi dolore!
          </q-card-section>

          <q-card-section class="q-pt-none">
            <div class="text-subtitle1">$・Italian, Cafe</div>
            <div class="text-caption text-grey">
              Small plates, salads & sandwiches in an intimate setting.
            </div>
          </q-card-section>

          <q-separator />

          <q-card-actions>
            <q-btn flat round icon="event" />
            <q-btn flat color="primary"> Reserve </q-btn>
          </q-card-actions>
        </app-card>
      </div>

      <div class="col-3">
        <app-card>
          <q-card-section>
            <q-btn
              fab
              color="primary"
              icon="place"
              class="absolute"
              style="top: 0; right: 12px; transform: translateY(-50%)"
            />

            <div class="row no-wrap items-center">
              <div class="col text-h6 ellipsis">Cafe Basilico</div>
              <div
                class="
                  col-auto
                  text-grey text-caption
                  q-pt-md
                  row
                  no-wrap
                  items-center
                "
              >
                <q-icon name="place" />
                250 ft
              </div>
            </div>

            <q-rating v-model="stars" :max="5" size="32px" />
          </q-card-section>

          <q-card-section class="q-pt-none">
            <div class="text-subtitle1">$・Italian, Cafe</div>
            <div class="text-caption text-grey">
              Small plates, salads & sandwiches in an intimate setting.
            </div>
          </q-card-section>

          <q-separator />

          <q-card-actions>
            <q-btn flat round icon="event" />
            <q-btn flat color="primary"> Reserve </q-btn>
          </q-card-actions>
        </app-card>
      </div>

      <div class="col-3">
        <app-card>
          <q-card-section>
            <q-btn
              fab
              color="primary"
              icon="place"
              class="absolute"
              style="top: 0; right: 12px; transform: translateY(-50%)"
            />

            <div class="row no-wrap items-center">
              <div class="col text-h6 ellipsis">Cafe Basilico</div>
              <div
                class="
                  col-auto
                  text-grey text-caption
                  q-pt-md
                  row
                  no-wrap
                  items-center
                "
              >
                <q-icon name="place" />
                250 ft
              </div>
            </div>

            <q-rating v-model="stars" :max="5" size="32px" />
          </q-card-section>

          <q-card-section class="q-pt-none">
            <div class="text-subtitle1">$・Italian, Cafe</div>
            <div class="text-caption text-grey">
              Small plates, salads & sandwiches in an intimate setting.
            </div>
          </q-card-section>

          <q-separator />

          <q-card-actions>
            <q-btn flat round icon="event" />
            <q-btn flat color="primary"> Reserve </q-btn>
          </q-card-actions>
        </app-card>
      </div>

      <div class="col-3">
        <app-card>
          <q-card-section>
            <q-btn
              fab
              color="primary"
              icon="place"
              class="absolute"
              style="top: 0; right: 12px; transform: translateY(-50%)"
            />

            <div class="row no-wrap items-center">
              <div class="col text-h6 ellipsis">Cafe Basilico</div>
              <div
                class="
                  col-auto
                  text-grey text-caption
                  q-pt-md
                  row
                  no-wrap
                  items-center
                "
              >
                <q-icon name="place" />
                250 ft
              </div>
            </div>

            <q-rating v-model="stars" :max="5" size="32px" />
          </q-card-section>

          <q-card-section class="q-pt-none">
            <div class="text-subtitle1">$・Italian, Cafe</div>
            <div class="text-caption text-grey">
              Small plates, salads & sandwiches in an intimate setting.
            </div>
          </q-card-section>

          <q-separator />

          <q-card-actions>
            <q-btn flat round icon="event" />
            <q-btn flat color="primary"> Reserve </q-btn>
          </q-card-actions>
        </app-card>
      </div>

      <div class="col-5">
        <app-card>
          <q-card-section>
            <q-btn
              fab
              color="primary"
              icon="place"
              class="absolute"
              style="top: 0; right: 12px; transform: translateY(-50%)"
            />

            Lorem ipsum dolor sit amet consectetur adipisicing elit.
            Necessitatibus nostrum nihil

            <div class="row no-wrap items-center">
              <div class="col text-h6 ellipsis">Cafe Basilico</div>
              <div
                class="
                  col-auto
                  text-grey text-caption
                  q-pt-md
                  row
                  no-wrap
                  items-center
                "
              >
                <q-icon name="place" />
                250 ft
              </div>
            </div>

            <q-rating v-model="stars" :max="5" size="32px" />
          </q-card-section>

          <q-card-section class="q-pt-none">
            <div class="text-subtitle1">$・Italian, Cafe</div>
            <div class="text-caption text-grey">
              Small plates, salads & sandwiches in an intimate setting.
            </div>
          </q-card-section>

          <q-separator />

          <q-card-actions>
            <q-btn flat round icon="event" />
            <q-btn flat color="primary"> Reserve </q-btn>
          </q-card-actions>
        </app-card>
      </div>
    </div>
  </q-page>
</template>

<script lang="ts">
import { Todo, Meta } from 'components/models';
import { defineComponent, ref } from 'vue';
import AppCard from 'components/AppCard.vue';

export default defineComponent({
  name: 'PageIndex',
  components: { AppCard },
  setup() {
    const todos = ref<Todo[]>([
      {
        id: 1,
        content: 'ct1',
      },
      {
        id: 2,
        content: 'ct2',
      },
      {
        id: 3,
        content: 'ct3',
      },
      {
        id: 4,
        content: 'ct4',
      },
      {
        id: 5,
        content: 'ct5',
      },
    ]);
    const meta = ref<Meta>({
      totalCount: 1200,
    });
    return { todos, meta };
  },
});
</script>
