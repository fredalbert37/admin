<template>
  <q-layout view="hHh lpR fFf">
    <q-header elevated class="bg-primary text-white">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          @click="toggleLeftDrawer"
          aria-label="Menu"
          icon="fas fa-bars"
        />

        <q-toolbar-title> Admin QuasarVue </q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" side="left" overlay bordered>
      <!-- drawer content -->
      <q-scroll-area
      style="
          height: calc(100% - 150px);
          margin-top: 150px;
          border-right: 1px solid #ddd;
          display: flex !important;
          flex-direction: column !important;
          flex-shrink: 0 !important;
      "
      >
        <EssentialLinks 
          v-for="(item, index) in router_list"
          :link="item.link"
          :icon="item.icon"
          :title="item.title"
          :active="item.active"
          :key="index"
        />
        <q-separator></q-separator>
        <q-list>
            <q-item clickable v-ripple>
            <q-item-section avatar>
                <q-icon name="fas fa-sign-out-alt" />
            </q-item-section>
            <q-item-section>Salir</q-item-section>
            </q-item>
        </q-list>
      </q-scroll-area>
      <q-img
        class="absolute-top"
        src="https://cdn.quasar.dev/img/material.png"
        style="height: 150px"
      >
        <div
          class="absolute-bottom bg-transparent flex items-center justify-center"
        >
          <q-avatar size="70px" class="q-mb-sm">
            <img src="https://cdn.quasar.dev/img/boy-avatar.png" />
          </q-avatar>
          <div class="q-ml-md">
            <div class="text-weight-bold text-h6">Administrador</div>
            <div>admin@admin.com</div>
          </div>
        </div>
      </q-img>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";
import EssentialLinks from "./components/EssentialLinks.vue";
import {router_list} from './router/router-list'

export default defineComponent({
  name: "LayoutDefault",

  components: {
    EssentialLinks
  },

  setup() {
    const leftDrawerOpen = ref(true);
    
    return {
      router_list,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
