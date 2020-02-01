<template>
      <v-card dark>
          <v-toolbar>
              <v-layout row>
                  <v-layout class="col-7">
                      <v-btn text class="mt-9" @click.stop ="drawer = !drawer">
                        <v-icon icon>mdi-menu</v-icon>
                        </v-btn>
                        <v-toolbar-title class="ml-lg-12 mt-10">K.I.Tist</v-toolbar-title>
                  </v-layout>
                  <v-layout class="col-4 mt-7">
                        <v-text-field
                        outlined=""
                        append-icon="mdi-magnify left"
                        label="Search"
                        />

                        <v-btn text class="mt-2 ml-lg-3">
                            <v-icon>mdi-bell-ring-outline</v-icon>
                        </v-btn>

                        <v-dialog
                            v-model="dialog"
                            width="400"
                            class="dialog"
                            persistent
                            >
                        <template v-slot:activator="{ on }">
                            <v-btn
                            dark
                            v-on="on"
                            text
                            class="mt-2">
                            <v-icon>mdi-account-box</v-icon>
                            </v-btn>
                        </template>
                        <Login/>
                        <v-btn  color="black grey--text" @click="dialog = false">
                            <v-icon>mdi-arrow-left</v-icon>
                        </v-btn>
                    </v-dialog>
                  </v-layout>
              </v-layout>
          </v-toolbar>
          <v-navigation-drawer
            v-model="drawer"
            app
            :mini-variant.sync="mini">
            <v-list-item class="px-2">
            <v-list-item-title>Task</v-list-item-title>

            <v-btn
              icon
              @click.stop="mini = !mini"
            >
              <v-icon>mdi-chevron-left</v-icon>
            </v-btn>
        </v-list-item>
        <hr>
           <NavDrawer/>

          </v-navigation-drawer>
      </v-card>
</template>

<script>
import Login from '../components/Login';
import NavDrawer from '../view/NavDrawer';
export default {
    name : 'NavBar',
    components : {
        NavDrawer,
        Login,
    },
    data (){
        return{
            drawer : false,
            dialog: false,
            mini : true
        }
    }
}
</script>

<style>
</style>