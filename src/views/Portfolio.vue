<template>
  <div class="portfolio">
    <v-containter>
      <h4 class="deep-purple--text text--lighten-3">
        “Learning is a treasure that will follow its owner everywhere.” —
        Chinese Proverb
      </h4>
      <v-spacer class="ma-6"></v-spacer>
      <!-- First Card -->
      <v-row class="mb-7" no-gutters>
        <v-col md="6" offset-md="3">
          <v-card class="mx-auto" max-width="700">
            <v-row>
              <v-col class="ma-3" md="3" cols="2">
                <v-img
                  class="rounded"
                  max-height="350"
                  max-width="100"
                  src="../assets/diveBandGig.png"
                ></v-img>
              </v-col>
              <v-col class="blue-grey--text text--darken-2">
                <v-card-text>
                  <h1>Dive</h1>
                  <v-spacer class="ma-2"></v-spacer>
                  <h3>
                    Dive is a mobile application that allows users to find local
                    bands. The user can follow bands, see a band's upcoming
                    shows or view a band's info. A user can also search upcoming
                    shows by venues. The app also allows for local bands reach
                    new fans by having a profile that lists their upcoming
                    shows.
                  </h3>
                </v-card-text>
              </v-col>
            </v-row>
            <h4>Tech Stack</h4>
            <v-row>
              <v-col cols="2"></v-col>
              <v-col cols="5">
                <v-list class="pa-md-4 mx-lg-auto">
                  <li class="text-sm-left">React Native</li>
                  <li class="text-sm-left">Expo</li>
                  <li class="text-sm-left">OAuth</li>
                  <li class="text-sm-left">Sequelize</li>
                  <li class="text-sm-left">NodeJS</li>
                </v-list>
              </v-col>
              <v-col cols="5">
                <v-list class="pa-md-4 mx-lg-auto">
                  <li class="text-sm-left">Express</li>
                  <li class="text-sm-left">MySQL</li>
                  <li class="text-sm-left">Sequelize</li>
                  <li class="text-sm-left">Google Cloud SQL</li>
                  <li class="text-sm-left">Google App Engine</li>
                </v-list>
              </v-col>
            </v-row>

            <div style="font-size: 1rem;">
              <a
                class="btn btn-large btn-primary logout"
                href="https://github.com/JoyPalumbo/Dive"
              >
                <i class="fa fa-github" left aria-hidden="true"> Dive Repo</i>
              </a>
            </div>
          </v-card>
        </v-col>
      </v-row>

      <!-- New Card -->
      <v-row class="mb-6" no-gutters>
        <v-col md="6" offset-md="3">
          <v-card class="mx-auto" max-width="700">
            <v-row>
              <v-card-text>
                <h1 class="blue-grey--text text--darken-2">Trivia App</h1>
              </v-card-text>
            </v-row>
            <v-row>
              <v-col class="ma-3" md="3" cols="2">
                <v-img
                  class="rounded"
                  max-height="350"
                  max-width="100"
                  src="../assets/triviaPhotoResize.jpg"
                ></v-img>
              </v-col>

              <v-col class="blue-grey--text text--darken-2" cols="8">
                <!-- <v-card-text> -->
                <!-- <v-spacer class="ma-2"></v-spacer> -->
                <!-- <v-row> -->
                <h4>
                  I have created two different trivia apps. The first app was
                  created for a coding challange, using a pre-made set of
                  trivia. When the user clicks on their answer they are shown
                  the correct and incorrect answers. They can click next to
                  progress to the next question. When they have answered the
                  last question they are shown their score.
                </h4>
              </v-col>
            </v-row>
            <v-row>
              <v-col cols="1"></v-col>
              <v-col class="blue-grey--text text--darken-2" cols="10">
                <h4>
                  The second app is an mvp, created in 24 hours. It utilizes an
                  external triva API. A user can select their answer and the app
                  keeps track of the users score. The user can click on a button
                  to see the correct answer. They can also vote for their
                  favorite questions and the app displays the top rated
                  questions.
                </h4>
              </v-col>
            </v-row>
            <!-- </v-card-text> -->
            <!-- </v-col> -->
            <!-- </v-row> -->
            <v-row>
              <!-- <v-col> -->
              <v-card-text>
                <h4>Tech Stack</h4>
              </v-card-text>
            </v-row>
            <v-row>
              <v-col cols="2"></v-col>
              <v-col>
                <v-list class="pa-md-4 mx-lg-auto">
                  <li class="text-sm-left">ReactJS</li>
                  <li class="text-sm-left">BootStrap</li>
                  <li class="text-sm-left">Axios</li>
                </v-list>
              </v-col>
              <v-col>
                <v-list class="pa-md-4 mx-lg-auto">
                  <li class="text-sm-left">Express</li>
                  <li class="text-sm-left">NodeJS</li>
                  <li class="text-sm-left">MySQL</li>
                </v-list>
              </v-col>

              <!-- </v-col> -->
            </v-row>
            <v-row>
              <v-col>
                <div style="font-size: 1rem;">
                  <a
                    class="btn btn-large btn-primary logout"
                    href="https://github.com/JoyPalumbo/tandem_trivia/tree/master"
                  >
                    <i class="fa fa-github" left aria-hidden="true">
                      First Trivia Repo</i
                    >
                  </a>
                </div>
              </v-col>
              <v-col>
                <div style="font-size: 1rem;">
                  <a
                    class="btn btn-large btn-primary logout"
                    href="https://github.com/JoyPalumbo/mvp-nov-19"
                  >
                    <i class="fa fa-github" left aria-hidden="true">
                      Second Trivia Repo</i
                    >
                  </a>
                </div>
              </v-col>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
      <v-row>
        <v-col>
          <h6>-This portolio made with VueJS, Vue Router and Vuetify</h6>
        </v-col>
      </v-row>
    </v-containter>
  </div>
</template>
