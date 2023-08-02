<template>
  <q-layout view="hHh lpR fFf">
    <q-header class="bg-dark text-white flex flex-center">
      <q-toolbar>
        <q-toolbar-title class="row flex-center">
          <q-avatar>
            <img :src="rocket" />
          </q-avatar>
          <h1 class="inter-bold text-primary">
            to<span class="text-accent">do</span>
          </h1>
        </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container class="flex flex-center">
      <q-page>
        <div class="flex q-gutter-md">
          <q-input
            class="col-grow"
            bg-color="grey-6"
            filled
            v-model="ph"
            placeholder="Placeholder"
            :dense="dense"
          ></q-input>
          <q-btn
            color="indigo-12"
            icon-right="add_circle_outline"
            label="Добавить"
          ></q-btn>
        </div>
      </q-page>
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
import rocket from "../assets/rocket.svg";

export default defineComponent({
  name: "MainLayout",

  setup() {
    return {
      rocket,
      ph: ref(""),
      dense: ref(false),
    };
  },
});
</script>

<style lang="scss">
.q-header {
  min-height: 200px;
}

.q-avatar {
  margin-right: 5px;
}

h1 {
  font-size: 3rem;
  line-height: 3rem;
}

.q-page {
  width: 100%;
  max-width: 768px;
}

.q-field__native {
  color: $grey-2;
}
</style>
