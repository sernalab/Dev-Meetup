<template>
  <v-container>
	<v-layout row wrap>
	  <v-flex xs12 sm6 class="text-xs-center text-sm-right">
		<v-btn large router to="/meetups" class="info">Explore Meetups</v-btn>
	  </v-flex>
	  <v-flex xs12 sm6 class="text-xs-center text-sm-left">
		<v-btn large router to="/meetup/new" class="info">Organize Meetup</v-btn>
	  </v-flex>
	</v-layout>
	<v-layout>
	  <v-flex xs12>
		<v-carousel>
		  <v-carousel-item 
		  v-for="meetup in meetups" 
		  :src="meetup.imageUrl" 
		  :key="meetup.id">
		  <div class="title">
		  	{{ meetup.title }}
		  </div>
		  </v-carousel-item>
		</v-carousel>
	  </v-flex>
	</v-layout>
  </v-container>
</template>

<script>
export default {
  data () {
    return {
      meetups: [
        {imageUrl: 'https://thenypost.files.wordpress.com/2017/04/new-york.jpg?quality=90&strip=all&w=1200', id: 'asdasd', title: 'Meetup in NY'},
        {imageUrl: 'https://pbs.twimg.com/media/C6jTt1wU8AEd0_4.jpg', id: 'asdasd', title: 'Meetup in Skylab'},
        {imageUrl: 'https://static04.ofertia.com/poblaciones/barcelona/barcelona/extra1-1115.v40.jpg', id: 'asdasd', title: 'Meetup in Barcelona'}
      ]
    }
  }
}
</script>

<style scoped>
	.title{
		position: absolute;
		bottom: 50px;
		background-color: rgba(0, 0, 0, 0.5);
		color: white;
		font-size: 2em;
		padding: 10px;
	}
</style>
