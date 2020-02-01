<template>
     <v-layout justify-center class="mt-12 mb-12">
        <v-card width="400px" height="auto" dark>
            <div class="mt-4 mb-4 mx-auto ml-4 mr-4" >
            <h1>ADD TASK</h1>
            <div class="ml-2 mr-2 pt-2" >
                <v-text-field label="Task name" :rules="rules" hide-details="auto" prepend-icon="notes"></v-text-field>
                <v-text-field label="Task description" prepend-icon="description"></v-text-field>
                <v-text-field type="date" label="Date" prepend-icon="event"></v-text-field>
                <v-layout justify-end>
                    <v-btn  color="primary">Save</v-btn>
                </v-layout>
            </div>
        </div>
    </v-card>
    </v-layout>
</template>

