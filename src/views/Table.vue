<template>
  <v-container>
    <v-row>
      <v-col cols="12">
  
  <v-data-table
    :headers="headers"
    :items="users"
    :items-per-page="5"
    class="elevation-1 mt-12" >
  
  <template slot="items" slot-scope="props">
                    
          <td>{{ props.item.username }}</td>
          <td class="text-xs-right">{{ props.item.email }}</td>
          <td class="text-xs-right">{{ props.item.phone }}</td>
          <td class="text-xs-right">{{ props.item.website }}</td>
                 
 </template>
                  
                  
</v-data-table>

      </v-col>
    </v-row>

  </v-container>



</template>

<script>
import axios from 'axios';
  export default {
    data () {
      return {
        headers: [
          {
            text: 'Username',
            align: 'start',
            sortable: false,
            value: 'username',
          },
          { text: 'Email', value: 'email' },
          { text: 'Phone', value: 'phone' },
          { text: 'Website', value: 'website' }
          
        ],
        users: [],
      }
    },

       created (){
       this.desserts= axios.get('https://jsonplaceholder.typicode.com/users')
        .then(res => this.users =res.data)
        .catch(err => console.log(err));

      }
  }


  
</script>
