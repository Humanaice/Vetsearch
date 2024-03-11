<template>
  <NuxtLayout>
    <div>
      <p>Hello World</p>
      <i class="fa-solid fa-user"></i>
    </div>
    <v-expansion-panels>
      <v-expansion-panel title="Title"
        text="Lorem ipsum dolor sit amet consectetur adipisicing elit. Commodi, ratione debitis quis est labore voluptatibus! Eaque cupiditate minima">
      </v-expansion-panel>
    </v-expansion-panels>
    <div class="text-center">
      <v-menu open-on-hover location="bottom center">
        <template v-slot:activator="{ props }">
          <v-btn color="primary" v-bind="props">
            Dropdown
          </v-btn>
        </template>

        <v-list>
          <v-list-item v-for="(item, index) in items" :key="index">
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </div>
  </NuxtLayout>
</template>

<script>
export default {
  data: () => ({
    items: [
      { title: 'Click MeAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAa' },
      { title: 'Click Me' },
      { title: 'Click Me' },
      { title: 'Click Me 2' },
    ],
  }),
}
</script>

<style scoped>
.page {
  background-color: white;
}
</style>
