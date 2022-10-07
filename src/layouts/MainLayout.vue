<template>
  <q-layout view="hHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="mdi-menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title>
          Quasar App
        </q-toolbar-title>

        <q-btn
          flat
          round
          icon="mdi-logout"
        />
      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      class="bg-grey-l"
    >
      <q-toolbar class="bg-primary" />
      <q-item class="bg-grey-3">
        <q-item-section>
          Listt
        </q-item-section>
        <q-item-section side>
          <CreateTodoListButton
            icon="mdi-plus"
            size="sm"
            flat
            round
          />
        </q-item-section>
      </q-item>
      <TodoListsList />
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'
import CreateTodoListButton from '../components/CreateTodoListButton.vue'
import TodoListsList from 'src/components/TodoListsList.vue'

export default defineComponent({
  components: { CreateTodoListButton, TodoListsList },
  setup () {
    const leftDrawerOpen = ref(false)
    return {
      leftDrawerOpen,
      toggleLeftDrawer () {
        leftDrawerOpen.value = !leftDrawerOpen.value
      }
    }
  }
})
</script>
