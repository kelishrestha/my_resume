<template>
    <v-navigation-drawer app dark :width="width" :value="true" stateless class="teal">
      <v-img src="https://scontent.fktm3-1.fna.fbcdn.net/v/t31.0-8/22555553_10208674443253424_8742489099592047203_o.jpg?_nc_cat=102&_nc_eui2=AeEr-iuupbxY4ZwqmBHLUOysOMljl3_W2t59oVdSNY3GKwwYsC-gmiMJ-I_Ifh5IjBbY7vaDFyvJGa8L3EOcMMCdyyxCVhaG20qhqVSTgKmGzw&_nc_ht=scontent.fktm3-1.fna&oh=47c3cbd7e6498ddee25c44311dc25ec6&oe=5D0D31AC">
        <v-layout pa-2 column fill-height class="lightbox white--text">
          <v-spacer></v-spacer>
          <v-flex shrink>
            <div class="subheading">{{ name }}</div>
            <div class="body-1">{{ email }}</div>
          </v-flex>
        </v-layout>
      </v-img>

      <v-list>
        <template v-for="(item, i) in items">
          <v-divider v-if="item.divider" :key="i"></v-divider>
          <v-list-tile v-else :key="item.title">
            <v-list-tile-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-tile-action>
            <v-list-tile-title>{{ item.title }}</v-list-tile-title>
          </v-list-tile>
        </template>
      </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
  name: 'SideBar',
  props: {
    name: String,
    email: String
  },
  data: () => ({
    width: 300,
    items: [
      { icon: 'home', title: 'Bhaktapur, Nepal' },
      { icon: 'phone', title: '+9779860790767' },
      { icon: 'mail', title: 'kelishrestha97@gmail.com' },
      { divider: true },
      { icon: 'delete', title: 'Trash' },
      { icon: 'error', title: 'Spam' }
    ]
  })
}
</script>

<style scoped>
  .v-navigation-drawer {
    transition: none !important;
  }

  .lightbox {
    box-shadow: 0 0 20px inset rgba(0, 0, 0, 0.2);
    background-image: linear-gradient(to top, rgba(0, 0, 0, 0.4) 0%, transparent 72px);
  }
</style>
