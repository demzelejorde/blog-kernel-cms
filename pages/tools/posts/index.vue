<template>
  <div>
    <h1 class="title">
      Posts
    </h1>
    <br>
    <v-data-table :headers="headers" :items="posts">
      <template slot="items" slot-scope="props">
        <td>{{ props.item.title }}</td>
        <td class="text-xs-center">{{ props.item.section }}</td>
        <td class="text-xs-center">{{ props.item.author }}</td>
        <td class="text-xs-center">{{ props.item.date_published }}</td>
      </template>
    </v-data-table>
  </div>
</template>

<script>
// import AppLogo from '~/components/AppLogo.vue'

export default {
  data() {
    return { 
      headers: [
        { text: 'Title', align: 'left', value: 'title'},
        { text: 'Section', align: 'center', sortable: false, value: 'section'},
        { text: 'Author', align: 'center', sortable: false, value: 'author'},
        { text: 'Date Published', align: 'center', value: 'date_published'}
      ],
      posts : [
        {
          title : 'Ford cars with SYNC 3 can now project Waze from their screens',
          section : 'Technology News',
          author : 'Jason Tulio',
          date_published : 'May 18, 2018'
        },
        {
          title : 'The Nissan Armada \'Mountain Patrol\' is a campsite on wheels',
          section : 'Car News',
          author : 'Drei Laurel',
          date_published : 'May 18, 2018'
        },
        {
          title : 'Top 5 expenses first-time car owners don’t anticipate',
          section : 'Advertorial',
          author : 'Topgear.com.ph',
          date_published : 'May 16, 2018'
        },
        {
          title : 'The new and improved Toyota Alphard is now in PH',
          section : 'Car News',
          author : 'Drei Laurel',
          date_published : 'May 16, 2018'
        },
        {
          title : 'Meet the man behind the Rainforest Challenge',
          section : 'Feature Article',
          author : 'Paulo Rafael Subido',
          date_published : 'May 16, 2018'
        },
        {
          title : 'This replica McLaren racing wheel will make any gamer]\'s jaw drop',
          section : 'Toys',
          author : 'Mike Channell',
          date_published : 'May 16, 2018'
        },
        {
          title : 'The Ford Mustang convertible is fiery passion personified',
          section : 'Feature Article',
          author : 'Jason Tulio',
          date_published : 'May 16, 2018'
        },
        {
          title : '5 Reasons to visit Trans Sport Show 2018',
          section : 'Feature Article',
          author : 'Paulo Rafael Subido',
          date_published : 'May 15, 2018'
        },
        {
          title : 'Mini has prepared a special Hatch for Prince Harry and Meghan Markle',
          section : 'Car News',
          author : 'Drei Laurel',
          date_published : 'May 15, 2018'
        },
        {
          title : 'The Aston Martin DB11 AMR is the brand\'s new flagship car',
          section : 'Car News',
          author : 'Jack Rix',
          date_published : 'May 15, 2018'
        },
      ]
    }
  }
}
</script>