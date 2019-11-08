<template>
  <v-app id="inspire" color="light">
    <v-app-bar app color="primary">
      <v-toolbar-title class="headline text-uppercase">
        <span color="primary">Vuetify</span>
        <span class="font-weight-light">MATERIAL DESIGN</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">Latest Release</span>
      </v-btn>
    </v-app-bar>

    <v-content>
      <v-tabs-items v-model="tab">
        <v-tab-item
          v-for="(item, index) in items"
          :key="index"
        >
          <div class="">{{item.name}}のchart.jsが入る</div>
          <v-card>
            <v-card-title>以下に売上履歴が入る</v-card-title>
            <v-card-text>{{item.text}}</v-card-text>
          </v-card>
        </v-tab-item>
      </v-tabs-items>
    </v-content>
    <v-card color="basil">
      <v-tabs
        v-model="tab"
        background-color="transparent"
        color="basil"
        class="mb-1"
        grow
      >
        <v-tab
          v-for="(item, index) in items"
          :key="index"
        >
          {{ item.name }}
        </v-tab>
      </v-tabs>

    </v-card>
  </v-app>
</template>

<script>
// import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    // HelloWorld
  },
  data: () => ({
    tab:null,
    items:[
      {
        name:'tab1',
        text:'hogehogehogehoge'
      },
      {
        name:'tab2',
        text:'fugafugafugafuga'
      }
    ]
  }),
};
</script>