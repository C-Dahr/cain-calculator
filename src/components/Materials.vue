<template>
  <v-card color="brown" dark class="elevation-10">
    <v-card-title>
      Materials
    </v-card-title>
    <v-card-text>
      Click on a material below to add it to the bag of crafting.
      <v-row justify="center" align="center">
        <v-col v-for="(item,index) in materialKey.slice(0,5)" v-bind:key="item.name" cols="2">
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-btn text large>
                <v-img
                  v-bind:src="require('../assets/pickups/' + item.icon)"
                  @click="addItem(index+1)"
                  v-bind="attrs"
                  v-on="on">
                </v-img>
              </v-btn>
            </template>
            <span>{{item.name}}</span>
          </v-tooltip>
        </v-col>
      </v-row>
      <v-row justify="center" align="center">
        <v-col v-for="(item,index) in materialKey.slice(5,10)" v-bind:key="item.name" cols="2">
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-btn text large>
                <v-img
                  v-bind:src="require('../assets/pickups/' + item.icon)"
                  @click="addItem(index+6)"
                  v-bind="attrs"
                  v-on="on">
                </v-img>
              </v-btn>
            </template>
            <span>{{item.name}}</span>
          </v-tooltip>
        </v-col>
      </v-row>
      <v-row justify="center" align="center">
        <v-col v-for="(item,index) in materialKey.slice(10,15)" v-bind:key="item.name" cols="2">
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-btn text large>
                <v-img
                  v-bind:src="require('../assets/pickups/' + item.icon)"
                  @click="addItem(index+11)"
                  v-bind="attrs"
                  v-on="on">
                </v-img>
              </v-btn>
            </template>
            <span>{{item.name}}</span>
          </v-tooltip>
        </v-col>
      </v-row>
      <v-row justify="center" align="center">
        <v-col v-for="(item,index) in materialKey.slice(15,20)" v-bind:key="item.name" cols="2">
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-btn text large>
                <v-img
                  v-bind:src="require('../assets/pickups/' + item.icon)"
                  @click="addItem(index+16)"
                  v-bind="attrs"
                  v-on="on">
                </v-img>
              </v-btn>
            </template>
            <span>{{item.name}}</span>
          </v-tooltip>
        </v-col>
      </v-row>
      <v-row justify="center" align="center">
        <v-col v-for="(item,index) in materialKey.slice(20,25)" v-bind:key="item.name" cols="2">
          <v-tooltip bottom>
            <template v-slot:activator="{ on, attrs }">
              <v-btn text large>
                <v-img
                  v-bind:src="require('../assets/pickups/' + item.icon)"
                  @click="addItem(index+21)"
                  v-bind="attrs"
                  v-on="on">
                </v-img>
              </v-btn>
            </template>
            <span>{{item.name}}</span>
          </v-tooltip>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>

<script>

export default {
  name: 'Materials',
  components: {
  },
  props: {
    materialKey: Array
  },
  data: () => ({
  }),
  methods: {
    addItem (id) {
      this.$emit('add', id)
    }
  }
}
</script>
