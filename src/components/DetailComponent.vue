<template>
  <v-layout align-center>
    <v-item-group v-model="window" class="shrink mr-4" mandatory tag="v-flex">
      <v-item v-for="(item, i) in items">
        <div slot-scope="{ active, toggle }">
          <v-btn :input-value="active" @click="toggle">
            <v-icon>{{ item.icon }}</v-icon>
            <strong class="title">{{ item.title }}</strong>
          </v-btn>
        </div>
      </v-item>
    </v-item-group>

    <v-flex>
      <v-window v-model="window" class="elevation-1" vertical>
        <v-window-item v-for="(item, i) in items">
          <v-card flat>
            <v-card-text>
              <v-layout align-center mb-3>
                <strong class="title">{{ item.title }}</strong>
                <v-spacer></v-spacer>
                <v-btn icon>
                  <v-icon>{{ item.icon }}</v-icon>
                </v-btn>
              </v-layout>

              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
              </p>

              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
              </p>

              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
              </p>
            </v-card-text>
          </v-card>
        </v-window-item>
      </v-window>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    name: 'DetailComponent',
    data: () => ({
      window: 0,
      items: [
        { icon: 'home', title: 'Experience' },
        { icon: 'phone', title: 'Education' },
        { icon: 'mail', title: 'Skills' }
      ]
    })
  }
</script>
