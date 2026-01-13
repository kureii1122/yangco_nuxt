<template>

   <v-container fluid>
    <v-app>

      <!-- Navbar -->

      <v-navigation-drawer>

<v-list>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            subtitle="sandra_a88@gmailcom"
            title="Sandra Adams"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>

          <v-list-item prepend-icon="mdi-folder" title="Dashboard" value="dashboard"></v-list-item>
          <v-list-item prepend-icon="mdi-list-box" title="Inventory" value="inventory"></v-list-item>
          <v-list-item prepend-icon="mdi-view-list" title="Category" value="category"></v-list-item>
          <v-list-item prepend-icon="mdi-account-circle" title="Users" value="users"></v-list-item>
        </v-list>
     </v-navigation-drawer>

     <!-- App bar -->
      <v-app-bar :elevation="2">
  <template v-slot:prepend>
    <v-app-bar-nav-icon @click.stop="drawer =! drawer"></v-app-bar-nav-icon>
  </template>

  <v-app-bar-title>Inventory Management System</v-app-bar-title>
</v-app-bar>
<v-main>
  <slot/>
</v-main>

    </v-app>
  
    </v-container>
</template>


<script setup>
  const drawer = ref(false)

</script>
<style></style>