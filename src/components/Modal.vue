<template>
  <v-dialog v-model="modalShow" max-width="900">
    <v-card>
      <v-card-title>
        <v-toolbar dense>
          <v-btn icon @click="closeModal">
            <v-icon>mdi-close</v-icon>
          </v-btn>
          <v-toolbar-title>Modal Title</v-toolbar-title>
          <v-spacer></v-spacer>
        </v-toolbar>
      </v-card-title>
      <v-card-text>
        <v-tabs v-model="tab" color="indigo" dark slider-color="yellow">
          <v-tab value="one">Item One</v-tab>
          <v-tab value="two">Item Two</v-tab>
          <v-tab value="three">Item Three</v-tab>
        </v-tabs>
      </v-card-text>
      <v-card-text>
        <v-window v-model="tab">
          <v-window-item value="one">
            <Tab1Content />
          </v-window-item>

          <v-window-item value="two">
            <Tab2Content />
          </v-window-item>

        </v-window>
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
import Tab1Content from './Tab1Content.vue'
import Tab2Content from './Tab2Content.vue'
export default {
  name: 'MyModal',
  props: {
    showModal: {
      type: Boolean,
      default: false
    }
  },
  components: {
    Tab1Content,
    Tab2Content
  },
  data() {
    return {
      modalShow: this.showModal,
      tab: 'one'
    }
  },
  watch: {
    showModal() {
      this.modalShow = this.showModal
    },
    modalShow() {
      this.$emit('update:showModal', this.modalShow)
    }
  },
  methods: {
    closeModal() {
      this.modalShow = false
      this.$emit('update:showModal', false)
    }
  }
}
</script>
