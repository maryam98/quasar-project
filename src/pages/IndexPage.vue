<template>
  <q-page class="row">
    <q-card class="col-xs-9">
      <q-toolbar>
        <q-input
          dense
          placeholder="search"
          borderless
          class="full-width"
          :model-value="search"
        >
          <template #append>
            <q-icon name="mdi-magnify" />
          </template>
        </q-input>
      </q-toolbar>
      <q-list bordered>
        <q-item>
          <q-item-section>
            <q-checkbox :model-value="true" />
          </q-item-section>

          <q-iteme-section>
            Go shoping now
          </q-iteme-section>

          <q-item-section side>
            <q-btn
              flat
              round
              size="sm"
              icon="mdi-delete"
            />
          </q-item-section>
        </q-item>
      </q-list>
    </q-card>
    <q-card class="col-xs-3">
      <q-toolbar class="bg-primary">
        <q-btn
          fab
          style="margin-bottom:-42px"
          class="q-ml-lg"
          color="secondary"
          icon="mdi-plus"
        />
      </q-toolbar>
    </q-card>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'

export default defineComponent({
  name: 'IndexPage',
  data () {
    return {
      search: ''
    }
  }

})
</script>
