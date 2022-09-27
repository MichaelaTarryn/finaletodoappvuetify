<template>
<div class="home">
  <v-list
  class="pt-0"
      flat

    >
    <div v-for="task in tasks" :key="tasks.id">
       <v-list-item >
          <template v-slot:default="{ active }">
            <v-list-item-action>
              <v-checkbox :input-value="task.done"></v-checkbox>
            </v-list-item-action>

            <v-list-item-content>
              <v-list-item-title>{{task.title}}</v-list-item-title>
              
            </v-list-item-content>
          </template>
        </v-list-item>
        <v-divider></v-divider>
    </div>
       

    </v-list>
</div>
</template>

<script>
import { fa } from 'vuetify/lib/locale';



  export default{
data(){
  return{
     tasks:[
      {
        id:1,
        title:'Wake up' ,
        done:false,
      },
      {
        id:2,
        title:'Get up' ,
        done:false,
      },
      {
        id:3,
        title:'Brush teeth' ,
        done:false,
      },
      {
        id:4,
        title:'SMILE' ,
        done:false,
      }
     ]
  }
 
}
  }

 
</script>
