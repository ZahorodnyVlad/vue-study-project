<template>
    <v-container>
        <v-layout row>
            <v-flex xs12 sm6 offset-sm3>
                <h1 class="text--secondary mb-3">My ads</h1>

                <v-card
                        class="elevation-10 mb-3"
                        v-for="ad in ads"
                        :key="ad.id"
                >

                    <v-layout row>
                        <v-flex xs4>
                            <v-card-media
                            :src="ad.imageSrc"
                            height="175"
                            >
                            </v-card-media>
                        </v-flex>
                        <v-flex xs8>
                            <v-card-text>
                                <h2 class="text--primary">{{ad.title}}</h2>
                                <p>{{ ad.description }}</p>
                            </v-card-text>
                            <v-card-actions>
                                <v-spacer></v-spacer>
                                <v-btn
                                        class="info"
                                        :to="'/ad/' + ad.id"
                                >Open</v-btn>
                            </v-card-actions>
                        </v-flex>
                    </v-layout>

                </v-card>

            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
  export default {
    data () {
      return {
        ads: [
          {
            title: 'first',
            description: 'first image',
            promo: false,
            imageSrc: 'http://opogode.ua/images/images/524328a760a5e0e716003394.jpg',
            id: '123'
          },
          {
            title: 'second',
            description: 'second image',
            promo: true,
            imageSrc: 'https://people.in.ua/wp-content/uploads/2017/02/sobaka-1-649x450.jpg',
            id: '1234'
          }
        ]
      }
    }
  }
</script>

<style scoped>

</style>