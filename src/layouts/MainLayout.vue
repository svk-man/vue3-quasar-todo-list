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

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import rocket from "../assets/rocket.svg";

export default defineComponent({
  name: "MainLayout",

  setup() {
    return { rocket };
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
</style>
