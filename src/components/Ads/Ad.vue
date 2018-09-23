<template>
    <v-container>
        <v-layout row>
            <v-flex xs12>
                <v-card>
                    <v-card-media
                        src="http://opogode.ua/images/images/524328a760a5e0e716003394.jpg"
                        height="300"
                    ></v-card-media>
                    <v-card-text>
                        <h1 class="text--primary">title</h1>
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Dignissimos, eos.</p>
                    </v-card-text>
                    <v-card-actions>
                        <v-spacer></v-spacer>
                        <v-btn class="warning" flat>Edit</v-btn>
                        <v-btn class="success">Buy</v-btn>
                    </v-card-actions>
                </v-card>
            </v-flex>
        </v-layout>
    </v-container>
</template>

<script>
  export default {
    data () {
      return {}
    }
  }
</script>

<style scoped>

</style>