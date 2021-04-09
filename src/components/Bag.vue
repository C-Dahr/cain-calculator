<template>
  <v-card color="brown" dark class="elevation-10">
    <v-card-title>
      Bag of Crafting
    </v-card-title>
    <v-card-text>
      <v-row justify="center" align="center" class="mb-5">
        <v-col cols=3>
          <v-img src="../assets/Bag_of_Crafting_icon.png" max-width="150"></v-img>
          <v-btn class="mr-2">
            Craft
          </v-btn>
          <v-btn @click="resetBag()">
            Reset
          </v-btn>
        </v-col>
        <v-col>
          <v-row justify="center" align="center">
            <v-col class="mr-0">
              <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                <v-card-text >
                  <div v-if="bag.length >= 1" class="mr-0">
                    <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[0]-1].icon)" max-width="50" class="mx-auto"></v-img>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
            <v-col>
              <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                <v-card-text>
                  <div v-if="bag.length >= 2">
                    <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[1]-1].icon)" max-width="50" class="mx-auto"></v-img>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
            <v-col>
              <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                <v-card-text>
                  <div v-if="bag.length >= 3">
                    <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[2]-1].icon)" max-width="50" class="mx-auto"></v-img>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
            <v-col>
              <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                <v-card-text>
                  <div v-if="bag.length >= 4">
                    <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[3]-1].icon)" max-width="50" class="mx-auto"></v-img>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
          <v-row>
            <v-col>
              <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                <v-card-text>
                  <div v-if="bag.length >= 5">
                    <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[4]-1].icon)" max-width="50" class="mx-auto"></v-img>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
            <v-col>
              <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                <v-card-text>
                  <div v-if="bag.length >= 6">
                    <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[5]-1].icon)" max-width="50" class="mx-auto"></v-img>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
            <v-col>
              <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                <v-card-text>
                  <div v-if="bag.length >= 7">
                    <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[6]-1].icon)" max-width="50" class="mx-auto"></v-img>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
            <v-col>
              <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                <v-card-text>
                  <div v-if="bag.length >= 8">
                    <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[7]-1].icon)" max-width="50" class="mx-auto"></v-img>
                  </div>
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-card-text>
  </v-card>
</template>

<script>

export default {
  name: 'Bag',
  components: {
  },
  props: {
    bag: Array,
    materialKey: Array
  },
  data: () => ({
  }),
  methods: {
    resetBag (id) {
      this.$emit('reset')
    }
  }
}
</script>
