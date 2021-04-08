<template>
  <v-container fill-height fluid>
    <v-row justify="center" align="center" class="mt-5">
      <v-col v-for="item in bag" v-bind:key="item.name">
        <v-img v-bind:src="require('../assets/pickups/' + materialKey[item-1].icon)" :key="item.name" max-width="50"></v-img>
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
