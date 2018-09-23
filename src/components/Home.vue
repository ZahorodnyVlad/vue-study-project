<template>

    <div>

        <v-container fluid>
            <v-layout row>
                <v-flex xs12>
                    <v-carousel>
                        <v-carousel-item
                                v-for="ad in ads"
                                :key="ad.id"
                                :src="ad.imageSrc"
                        >
                            <div class="link">
                                <v-btn class="error" :to="'/ad/' + ad.id">{{ ad.title }}</v-btn>
                            </div>
                        </v-carousel-item>
                    </v-carousel>
                </v-flex>
            </v-layout>
        </v-container>

        <v-container grid-list-lg>
            <v-layout row wrap>
                <v-flex xs12 sm6 md4 v-for="ad of ads" :key="ad.id">
                    <v-card>
                        <v-img
                                :src="ad.imageSrc"
                                height="200px"
                        ></v-img>

                        <v-card-title primary-title>
                            <div>
                                <h3 class="headline mb-0">{{ ad.title }}</h3>
                                <div>{{ ad.description }}</div>
                            </div>
                        </v-card-title>

                        <v-card-actions>
                            <v-spaser></v-spaser>
                            <v-btn flat :to="'/ad/' + ad.id">Open</v-btn>
                            <v-btn raised class="primary">Buy</v-btn>
                        </v-card-actions>
                    </v-card>
                </v-flex>
            </v-layout>
        </v-container>

    </div>


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
          },
          {
            title: 'third',
            description: 'third image',
            promo: true,
            imageSrc: 'https://img.depo.ua/745xX/Dec2015/79593.jpg',
            id: '12345'
          }
        ]
      }
    }
  }
</script>

<style scoped>

    .link {
        position: absolute;
        bottom: 50px;
        left: 50%;
        background-color: rgba(0,0,0,0.5);
        transform: translateX(-50%);
        padding: 5px 15px;
        border-top-left-radius: 5px;
        border-top-right-radius: 5px;
    }

</style>