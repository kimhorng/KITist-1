<template>
    <v-list dense>
        <v-list-item
          v-for="item in items"
          :key="item.title" router :to="item.route"
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
</template>
<script>
export default {
    name: 'Navbar',
    data(){
        return{
            items: [
          { title: 'Add Task', icon: 'add_circle' , route: '/addtask'},
          { title: 'Completed', icon: 'done_all' , route: '/completed'},
          { title: 'Important', icon: 'star' ,route: '/important'},
          { title: 'Dashboard', icon: 'dashboard',route:'/dashboard' },
          { title: 'Trash', icon: 'delete' ,route: '/trash'},
        ],
        mini: true,
        }
    },
  
}
</script>