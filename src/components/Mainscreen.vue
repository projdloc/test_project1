<template>
  <v-app>
    <v-toolbar color="indigo" dark fixed app>
      <v-toolbar-title>App Title</v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn text @click="openModal">Open Modal</v-btn>
    </v-toolbar>

    <v-content>
      <v-container fluid fill-height>
        <v-layout align-center justify-center>
          <v-card>
            <v-card-title>Page Content</v-card-title>
            <v-card-text>
              <p>Some content here</p>
            </v-card-text>
          </v-card>
        </v-layout>
      </v-container>
    </v-content>

    <MyModal v-model="modalShow"></MyModal>
  </v-app>
</template>

<script>
import MyModal from './Modal.vue'

export default {
  name: 'MyMainscreen',
  components: {
    MyModal
  },
  data() {
    return {
      modalShow: false
    }
  },
  methods: {
    openModal() {
      this.modalShow = true
    }
  }
}
</script>
