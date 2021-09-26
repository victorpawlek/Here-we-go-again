<template>
  <v-app>
    <v-card class="mx-auto" max-width="400">
      <v-img class="white--text align-end" height="200px" :src="car.image"> </v-img>
      <v-card-title>{{ car.title }}</v-card-title>

      <v-card-text>
        <p>
          Owner:
          <span class="font-weight-bold text--primary"
            >{{ car.owner.firstName }} {{ car.owner.lastName }}</span
          >
        </p>
        <p>
          Year: <span class="font-weight-bold text--primary">{{ car.yearOfMake }}</span
          ><br />Miles: <span class="font-weight-bold text--primary">{{ car.miles }}</span>
        </p>
        <p>
          Price: <span class="font-weight-bold text--primary">{{ car.price }}</span>
        </p>
        <p>
          {{ car.description }}
        </p>
      </v-card-text>

      <v-card-actions>
        <v-btn color="orange" text>
          Share
        </v-btn>

        <v-btn color="orange" text>
          Explore
        </v-btn>
      </v-card-actions>
    </v-card>
  </v-app>
</template>

<script>
export default {
  props: {
    car: {
      type: Object,
    },
  },
};
</script>

<style lang="scss" scoped></style>
