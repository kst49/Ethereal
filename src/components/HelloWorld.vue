<template>
  <v-container >
      <v-layout col>
        <v-flex offset-xs9>
          <v-card
              class="mx-auto"
              max-width="300"
          >
            <v-card-title>Reserve Tickets </v-card-title>
            <v-card-subtitle> Please select an available date & time </v-card-subtitle>
            <v-card-text class="text--primary">
              <v-col class="d-flex" sm="10">
                <v-select
                  :items="Object.keys(items)"
                  label="Available date & time"
                  v-model="item"
                ></v-select>
              </v-col>
            </v-card-text>
            <v-card-actions>
              <v-spacer> </v-spacer>
              <v-btn
                color="primary"
                :href= "items[item]"
              >
               Reserve
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>
  </v-container>
</template>

<script>
  export default {
    name: 'HelloWorld',
    data: () => ({
      item  :   'May 7th, 10am',
      items : { 'May 7th, 10am'   : 'https://www.eventbrite.com/e/tripple-tickets-96573376569', 
                'May 7th, 10:30am': 'https://www.eventbrite.com/e/tripple-tickets-96574417683', 
                'May 7th, 11am'   :'https://www.eventbrite.com/e/tripple-tickets-96574969333' }
    }),
  }
</script>


  