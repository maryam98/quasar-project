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
      <TodosList bordered />
    </q-card>
    <q-card class="col-xs-3">
      <q-toolbar class="bg-primary">
        <CreateTodoButton />
      </q-toolbar>
    </q-card>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import CreateTodoButton from 'src/components/CreateTodoButton.vue'
import TodosList from 'src/components/TodosList.vue'
export default defineComponent({
  name: 'IndexPage',
  components: {
    CreateTodoButton,
    TodosList
  },
  data () {
    return {
      search: ''
    }
  }

})
</script>
