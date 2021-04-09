<template>
  <v-container fill-height fluid>
    <v-row justify="center" align="center">
      <v-col cols=4>
        <Bag :bag="bagContents" :materialKey="materialKey" @reset="resetBag"/>
      </v-col>
    </v-row>
    <v-row justify="center" align="center">
      <v-col cols=4>
        <Materials :materialKey="materialKey" @add="addItem"/>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import Materials from '@/components/Materials.vue'
import Bag from '@/components/Bag.vue'

export default {
  name: 'Home',
  components: {
    Materials,
    Bag
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
  computed: {
    bagContents: function () {
      return this.bag
    }
  },
  methods: {
    addItem (id) {
      this.bag.push(id)
      if (this.bag.length >= 9) {
        this.bag.shift()
      }
    },
    resetBag () {
      this.bag = []
    }
  }
}
</script>
