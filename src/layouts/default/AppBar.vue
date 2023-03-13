<template>
  <v-app-bar
    color="whithe"
    prominent>
    <v-app-bar-nav-icon variant="text" @click.stop="drawer = !drawer" />


 
  </v-app-bar>

  <v-navigation-drawer
    v-model="drawer"
    location="left"
    temporary
  >
    <v-list-item
      title="Opciones"
    ></v-list-item>

    <v-divider></v-divider>

    <v-list density="compact" nav>
      <v-list-item @click="$router.push('/')"
        prepend-icon="mdi-view-dashboard"
        title="Home"
        value="value"
      ></v-list-item>

      <v-list-item @click="$router.push('tabla')"
        prepend-icon="mdi-table"
        title="Tabla"
        value="value"
      ></v-list-item>

      <v-list-item @click="$router.push('crud')"
        prepend-icon="mdi-table"
        title="Tabla CRUD"
        value="value"
      ></v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script setup>
  import { ref } from 'vue';

  const drawer = ref(false);
</script>
