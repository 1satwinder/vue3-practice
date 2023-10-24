<template>
    inside vuetify page
    <v-btn prepend-icon="$vuetify">hi</v-btn>
    <v-icon size="large" color="blue-darken-2" icon="mdi-message-text"></v-icon>
    <v-icon icon="mdi-success" />
    <br />
    <v-btn class="ma-2" color="primary">
        Accept
        <v-icon end icon="mdi-checkbox-marked-circle"></v-icon>
    </v-btn>
    <br />
    <v-card class="mx-auto" color="#26c6da" theme="dark" max-width="400" prepend-icon="mdi-twitter" title="Twitter">
        <template v-slot:prepend>
            <v-icon size="x-large"></v-icon>
        </template>

        <v-card-text class="text-h5 py-2">
            "Turns out semicolon-less style is easier and safer in TS because most gotcha edge cases are type invalid as
            well."
        </v-card-text>

        <v-card-actions>
            <v-list-item class="w-100">
                <template v-slot:prepend>
                    <v-avatar color="grey-darken-3"
                        image="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairShortCurly&accessoriesType=Prescription02&hairColor=Black&facialHairType=Blank&clotheType=Hoodie&clotheColor=White&eyeType=Default&eyebrowType=DefaultNatural&mouthType=Default&skinColor=Light"></v-avatar>
                </template>

                <v-list-item-title>Evan You</v-list-item-title>

                <v-list-item-subtitle>Vue Creator</v-list-item-subtitle>

                <template v-slot:append>
                    <div class="justify-self-end">
                        <v-icon class="me-1" icon="mdi-heart"></v-icon>
                        <span class="subheading me-2">256</span>
                        <span class="me-1">·</span>
                        <v-icon class="me-1" icon="mdi-share-variant"></v-icon>
                        <span class="subheading">45</span>
                    </div>
                </template>
            </v-list-item>
        </v-card-actions>
    </v-card>
    <v-card flat>
    <v-toolbar
      color="primary"
      dark
      extended
      flat
    >
      <v-app-bar-nav-icon></v-app-bar-nav-icon>
    </v-toolbar>

    <v-card
      class="mx-auto"
      max-width="700"
      style="margin-top: -64px;"
    >
      <v-toolbar flat>
        <v-toolbar-title class="text-grey">
          Title
        </v-toolbar-title>

        <v-spacer></v-spacer>

        <v-btn icon>
          <v-icon>mdi-magnify</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-apps</v-icon>
        </v-btn>

        <v-btn icon>
          <v-icon>mdi-dots-vertical</v-icon>
        </v-btn>
      </v-toolbar>

      <v-divider></v-divider>

      <v-card-text style="height: 200px;"></v-card-text>
    </v-card>
  </v-card>
</template>