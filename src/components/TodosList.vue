<template>
  <div>
    <q-list>
      <q-item>
        <q-item-section>
          <UpdateTodoCheckbox />
        </q-item-section>

        <q-iteme-section>
          Go shoping now
        </q-iteme-section>

        <q-item-section side>
          <DeleteTodoButton />
        </q-item-section>
      </q-item>
    </q-list>
  </div>
</template>

<script>
import UpdateTodoCheckbox from './UpdateTodoCheckbox.vue'
import DeleteTodoButton from './DeleteTodoButton'
export default {
  components: {
    UpdateTodoCheckbox,
    DeleteTodoButton
  }
  // name: 'ComponentName',

}
</script>
