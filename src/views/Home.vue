<template>
  <v-container fill-height fluid>
    <v-row justify="center" align="center">
      <v-col cols=6>
        <v-card color="brown" dark class="elevation-10">
          <v-card-title>
            Welcome to the Bag of Crafting Calculator
          </v-card-title>
          <v-card-text>
            <v-row justify="center" align="center">
              <v-col v-for="item in bag" :key="item.name">
                {{item.name}}
                <v-img src="item.path" max-width="50"></v-img>
              </v-col>
            </v-row>
            <v-row justify="center" align="center">
              <v-col cols="2">
                <v-img src="@/assets/pickups/Red_Heart.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Soul_Heart.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Black_Heart.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Eternal_Heart.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Gold_Heart.png" max-width="50"></v-img>
              </v-col>
            </v-row>
            <v-row justify="center" align="center">
              <v-col cols="2">
                <v-img src="@/assets/pickups/Bone_heart.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Rotten_Heart.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Penny.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Nickel.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Dime.png" max-width="50"></v-img>
              </v-col>
            </v-row>
            <v-row justify="center" align="center">
              <v-col cols="2">
                <v-img src="@/assets/pickups/Lucky_Penny.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Key.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Golden_Key.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Charged_Key.gif" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Bomb.png" max-width="50"></v-img>
              </v-col>
            </v-row>
            <v-row justify="center" align="center">
              <v-col cols="2">
                <v-img src="@/assets/pickups/Golden_Bomb.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Giga_Bomb.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Micro_Battery.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Lil_Battery.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Mega_Battery.png" max-width="50"></v-img>
              </v-col>
            </v-row>
            <v-row justify="center" align="center">
              <v-col cols="2">
                <v-img src="@/assets/pickups/TarotCard.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Pill_Black_White.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Rune1.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Pickup_Dice_Shard_icon.png" max-width="50"></v-img>
              </v-col>
              <v-col cols="2">
                <v-img src="@/assets/pickups/Pickup_Cracked_Key_icon.png" max-width="40"></v-img>
              </v-col>
            </v-row>
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  },
  data: () => ({
    bag: []
  })
}
</script>
