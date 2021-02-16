<template>
  <div>
    <v-row no-gutters class="mt-5">
      <v-col cols="12" sm="12" md="6">
        <v-card class="mx-auto pa-2" max-width="450">
          <v-img
            class="white--text"
            height="300px"
            src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
          >
          </v-img>
          <v-card-actions>
            <v-btn color="yellow lighten-1" class="ma-2 ">
              <v-icon right dark>
                mdi-share-variant
              </v-icon>
              SHARE
            </v-btn>

            <v-btn color="yellow lighten-1" class="ma-2 ">
              <v-icon right dark>
                mdi-cart
              </v-icon>
              ADD TO CART
            </v-btn>
            <v-btn  fab
            small
            class="ma-2 ">
              <v-icon right color="red">
                mdi-heart
              </v-icon>
            </v-btn>
          </v-card-actions>
        </v-card>
      </v-col>
      <v-col cols="6" md="6" class="text-center">
        <v-col cols="12" sm="8">
          <v-list>
            <v-list-item>
              <v-list-item-action>
                <h3>Name:</h3>
              </v-list-item-action>

              <h3>Lorem Ipsum</h3>
            </v-list-item>

            <v-list-item>
              <v-list-item-action>
                <h3>Price:</h3>
              </v-list-item-action>

              <h3>
                Rs.800 <sup><del>Rs.1000</del></sup>
                <span class="green--text"> 20% off</span>
              </h3>
            </v-list-item>

            <v-list-item>
              <v-list-item-action>
                <h3>Rating:</h3>
              </v-list-item-action>
              <v-rating
                :value="4.5"
                color="amber"
                dense
                half-increments
                readonly
                size="20"
              ></v-rating>
            </v-list-item>
            <v-list-item>
              <v-list-item-action>
                <h3>Size:</h3>
              </v-list-item-action>
              <v-chip-group
                v-model="selection"
                active-class="yellow lighten-1 accent-4 "
                column
              >
                <v-chip>Sm</v-chip>

                <v-chip>Md</v-chip>

                <v-chip>Xl</v-chip>
              </v-chip-group>
            </v-list-item>
            <v-list-item>
              <v-list-item-action>
                <h3>Color:</h3>
              </v-list-item-action>

              <v-list-item-title
                ><v-chip-group
                  v-model="selection"
                  active-class="yellow lighten-1 accent-4 "
                  column
                >
                  <v-chip>Red</v-chip>

                  <v-chip>Green</v-chip>

                  <v-chip>Blue</v-chip>
                </v-chip-group></v-list-item-title
              >
            </v-list-item>
          </v-list>
        </v-col>
      </v-col>
    </v-row>
 <h2 class="mt-5">Product Details</h2>
        <v-simple-table class="mt-5">
    <template v-slot:default>
      <tbody>
        <tr
          v-for="item in desserts"
          :key="item.name"
        >
          <td>{{ item.name }}</td>
          <td>{{ item.calories }}</td>
        </tr>
      </tbody>
    </template>
  </v-simple-table>
   <slider class="mt-5" />
  </div>
</template>

<script>
  export default {
    data () {
      return {
        desserts: [
          {
            name: 'Brand',
            calories: 159,
          },
          {
            name: 'City',
            calories: 237,
          },
          {
            name: 'Country',
            calories: 262,
          },
          {
            name: 'State',
            calories: 305,
          },
          {
            name: 'Area',
            calories: 356,
          },
          {
            name: 'Seller name',
            calories: 375,
          },
          {
            name: 'Description',
            calories: 392,
          },
          {
            name: 'Quantity',
            calories: 408,
          },
        ],
      }
    },
  }
</script>

<style></style>
