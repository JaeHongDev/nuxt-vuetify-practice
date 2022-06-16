<template>
  <v-menu>
    <template v-slot:activator="{ on, attrs }">
      <v-btn
        aria-expanded="false"
        aria-haspopup="true"
        role="button"
        type="button"
      >
        Click me
      </v-btn>
    </template>
      <v-select
        :items="['Foo', 'Bar']"
        label="Items"
      >


      </v-select>
    <v-list>

      <v-list-item @click="method">
        <v-list-item-title>Option 1</v-list-item-title>
      </v-list-item>

      <v-list-item disabled>
        <v-list-item-title>Option 2</v-list-item-title>
      </v-list-item>

      <v-list-item @click="method">
        <v-list-item-title>Option 3</v-list-item-title>
      </v-list-item>
    </v-list>

    <v-select
      :items="['Fizz', 'Buzz']"
      label="Items"
    >
      <template v-slot:item="{ item, attrs, on }">
        <v-list-item
          v-bind="attrs"
          v-on="on"
        >
          <v-list-item-content>
            <v-list-item-title
              :id="attrs['aria-labelledby']"
              v-text="item.title"
            ></v-list-item-title>

            <v-list-item-subtitle v-text="item.sub"></v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </template>
    </v-select>
  </v-menu>
</template>

<script>
export default {
  name: "Accessbility"
}
</script>

<style scoped>

</style>
