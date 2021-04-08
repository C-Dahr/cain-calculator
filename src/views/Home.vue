<template>
  <v-container fill-height fluid>
    <v-row justify="center" align="center">
      <v-col cols=6>
        <v-card color="brown" dark class="elevation-10">
          <v-card-title>
            Bag of Crafting
          </v-card-title>
          <v-card-text>
            <v-row>
              <v-col cols=2>
                <v-img src="../assets/Bag_of_Crafting_icon.png" max-width="150"></v-img>
              </v-col>
              <v-col>
                <v-row justify="center" align="center">
                  <v-col>
                    <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                      <v-card-text class="text-center">
                        <div v-if="bag.length >= 1">
                          <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[0]-1].icon)" max-width="50" class="mr-0"></v-img>
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-col>
                  <v-col>
                    <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                      <v-card-text class="text-center">
                        <div v-if="bag.length >= 2">
                          <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[1]-1].icon)" max-width="50"></v-img>
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-col>
                  <v-col>
                    <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                      <v-card-text class="text-center">
                        <div v-if="bag.length >= 3">
                          <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[2]-1].icon)" max-width="50"></v-img>
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-col>
                  <v-col>
                    <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                      <v-card-text class="text-center">
                        <div v-if="bag.length >= 4">
                          <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[3]-1].icon)" max-width="50"></v-img>
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-col>
                </v-row>
                <v-row>
                  <v-col>
                    <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                      <v-card-text class="text-center">
                        <div v-if="bag.length >= 5">
                          <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[4]-1].icon)" max-width="50"></v-img>
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-col>
                  <v-col>
                    <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                      <v-card-text class="text-center">
                        <div v-if="bag.length >= 6">
                          <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[5]-1].icon)" max-width="50"></v-img>
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-col>
                  <v-col>
                    <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                      <v-card-text class="text-center">
                        <div v-if="bag.length >= 7">
                          <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[6]-1].icon)" max-width="50"></v-img>
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-col>
                  <v-col>
                    <v-card color="#805a44" outlined height="100" width="100" style="border-color: #4f2d19">
                      <v-card-text class="text-center">
                        <div v-if="bag.length >= 8">
                          <v-img v-bind:src="require('../assets/pickups/' + materialKey[bag[7]-1].icon)" max-width="50"></v-img>
                        </div>
                      </v-card-text>
                    </v-card>
                  </v-col>
                </v-row>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
          </v-col>
        </v-row>
    <v-row justify="center" align="center">
      <v-col cols=6>
        <Materials :materialKey="materialKey" @add="addItem"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Materials from '@/components/Materials.vue'

export default {
  name: 'Home',
  components: {
    Materials
  },
  data: () => ({
    bag: [],
    materialKey: [
      {
        name: 'Red Heart',
        icon: 'Red_Heart.png'
      },
      {
        name: 'Soul Heart',
        icon: 'Soul_Heart.png'
      },
      {
        name: 'Black Heart',
        icon: 'Black_Heart.png'
      },
      {
        name: 'Eternal Heart',
        icon: 'Eternal_Heart.png'
      },
      {
        name: 'Gold Heart',
        icon: 'Gold_Heart.png'
      },
      {
        name: 'Bone Heart',
        icon: 'Bone_heart.png'
      },
      {
        name: 'Rotten Heart',
        icon: 'Rotten_Heart.png'
      },
      {
        name: 'Penny',
        icon: 'Penny.png'
      },
      {
        name: 'Nickel',
        icon: 'Nickel.png'
      },
      {
        name: 'Dime',
        icon: 'Dime.png'
      },
      {
        name: 'Lucky Penny',
        icon: 'Lucky_Penny.png'
      },
      {
        name: 'Key',
        icon: 'Key.png'
      },
      {
        name: 'Golden Key',
        icon: 'Golden_Key.png'
      },
      {
        name: 'Charged Key',
        icon: 'Charged_Key.gif'
      },
      {
        name: 'Bomb',
        icon: 'Bomb.png'
      },
      {
        name: 'Golden Bomb',
        icon: 'Golden_Bomb.png'
      },
      {
        name: 'Giga Bomb',
        icon: 'Giga_Bomb.png'
      },
      {
        name: 'Micro Battery',
        icon: 'Micro_Battery.png'
      },
      {
        name: "Lil' Battery",
        icon: 'Lil_Battery.png'
      },
      {
        name: 'Mega Battery',
        icon: 'Mega_Battery.png'
      },
      {
        name: 'Card',
        icon: 'TarotCard.png'
      },
      {
        name: 'Pill',
        icon: 'Pill_Black_White.png'
      },
      {
        name: 'Rune/Soul Gem',
        icon: 'Rune1.png'
      },
      {
        name: 'Dice Shard',
        icon: 'Pickup_Dice_Shard_icon.png'
      },
      {
        name: 'Cracked Key',
        icon: 'Pickup_Cracked_Key_icon.png'
      }
    ]
  }),
  methods: {
    addItem (id) {
      this.bag.push(id)
    }
  }
}
</script>
