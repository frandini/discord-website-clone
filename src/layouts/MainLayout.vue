<template>
  <q-layout view="hHh lpR fFf">

    <div class="main-background-color" style="display: flex; justify-content: center">
      <div class="q-px-xl max-content-width" style="width: 100%; height: 80px; display: flex; justify-content: space-between; align-items: center;">
        <router-link style="display: flex" :to="{ name: 'Home' }">
          <img src="~assets/discord_logo.svg" style="width: 134px; height: 34px"/>
        </router-link>
        <div v-if="$q.screen.gt.sm">
        <router-link v-for="(route, index) in routeLinks" :key="index" class="link" :to="{ name: route.name }">
          {{ route.label }}
        </router-link>
        </div>
        <div>
          <q-btn
            unelevated
            rounded
            color="white"
            class="text-capitalize"
            text-color="black"
            label="Abrir discord"
          />
          <q-btn
            v-if="$q.screen.lt.md"
            dense
            flat
            round
            color="white"
            icon="menu"
            class="q-ml-sm"
            @click="rightDrawerOpen = true"
            size="lg"
          />
        </div>
      </div>
    </div>

    <q-drawer v-model="rightDrawerOpen" side="right" overlay behavior="mobile" bordered>
      <div class="drawer">
        <div class="drawer-header">
          <router-link style="display: flex" :to="{ name: 'Home' }">
            <img src="~assets/discord_logo_black.svg" style="width: 134px; height: 34px"/>
          </router-link>
          <q-icon @click="rightDrawerOpen = false" class="cursor-pointer" name="close" size="sm" />
        </div>
        <q-separator />
        <router-link v-for="(route, index) in routeLinks" :key="index" class="link" :to="{ name: route.name }">
          {{ route.label }}
        </router-link>
        <q-space />
        <q-btn
            unelevated
            rounded
            icon="mdi-download-lock"
            class="text-capitalize download-btn"
            text-color="white"
            label="Baixar para windows"
          />
      </div>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
export default {
  name: 'MainLayout',
  data() {
    return {
      rightDrawerOpen: false,
      routeLinks: [
        { name: 'Download', label: 'Baixar'},
        { name: 'Nitro', label: 'Nitro'},
        { name: 'Download', label: 'Segurança'},
        { name: 'Download', label: 'Suporte'},
        { name: 'Download', label: 'Blog'},
        { name: 'Download', label: 'Carreiras'},
      ]
    }
  },
  mounted() {
    console.log('mounted', this.$q.screen);
  },
  methods: {
    clickBtn() {
      console.log('clicou');
    }
  }
}
</script>

<style scoped>
  .link {
    padding: 10px;
    margin: 0px 10px 0px 10px;
    color: white;
    text-decoration: none;
    font-family: Whitneysemibold;
    font-size: 16px;
    line-height: 22px;
  }

  .link:hover {
    text-decoration: underline;
  }

  .drawer {
    display: flex;
    flex-direction: column;
    padding: 24px;
    height: 100%;
  }

  .drawer .link {
    color: black;
    padding: 0px;
    margin: 10px;
  }

  .drawer-header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 24px;
  }

  .download-btn {
    background-color: #5865f2;
  }
</style>
