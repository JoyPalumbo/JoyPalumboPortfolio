<template>
  <v-container>
    <h4 class="deep-purple--text text--lighten-3">
      “I am learning all the time. The tombstone will be my diploma.” — Eartha
      Kitt
    </h4>
    <spacer class="ma-2"></spacer>
    <v-card class="mx-auto" max-width="450">
      <h3 class="blue-grey--text text--darken-2">
        Joy Palumbo
      </h3>
      <v-row>
        <v-col cols="12" sm="6" md="8">
          <v-card-text>
            <p class="text-sm-left">Phone: (818) 403-4577</p>
            <p class="text-sm-left">Email: greeniejoy@gmail.com</p>
          </v-card-text>
        </v-col>
        <v-col cols="6" md="4">
          <v-avatar size="75">
            <img src="../assets/profilePic.jpg" alt="Joy" />
          </v-avatar>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <a href="your link here">
            <div style="font-size: 1rem;">
              <a
                class="btn btn-large btn-primary logout"
                href="https://github.com/JoyPalumbo"
              >
                <i class="fa fa-github" left aria-hidden="true"> Github</i>
              </a>
            </div>
          </a>
        </v-col>

        <v-col>
          <a href="your link here">
            <div style="font-size: 1rem;">
              <a
                class="btn btn-large btn-primary logout"
                href="https://www.linkedin.com/in/joy-palumbo/"
              >
                <i class="fa fa-linkedin-square" aria-hidden="true">
                  Linked In</i
                >
              </a>
            </div>
          </a>
        </v-col>
      </v-row>
    </v-card>
    <spacer class="ma-2"></spacer>
  </v-container>
</template>
