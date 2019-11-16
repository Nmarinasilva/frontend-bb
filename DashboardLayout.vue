<template>
  <div class="wrapper" :class="{ 'nav-open': $sidebar.showSidebar }">
    <side-bar :background-color="sidebarBackground" short-title="Argon" title="Argon">
      <template slot="links">
        <sidebar-item
          :link="{
            name: 'Blackbook',
            icon: 'ni ni-single-copy-04 text-black',
            path: '/dashboard'
          }"
        />
        <sidebar-item
          :link="{name: 'Usuários', icon: 'ni ni-single-02 text-blue', path: '/icons'}"
        />
        <sidebar-item
          :link="{name: 'Adicionar Item', icon: 'ni ni-fat-add text-blue', path: '/register_produ'}"
        />
        <sidebar-item
          :link="{name: 'Retirar Item', icon: 'ni ni-cart text-blue', path: '/retira_produ'}"
        />
        <sidebar-item
          :link="{name: 'Histórico', icon: 'ni ni-archive-2 text-blue', path: '/profile'}"
        />
        <sidebar-item
          :link="{name: 'Categorias', icon: 'ni ni-bullet-list-67 text-blue', path: '/tables'}"
        />
        <sidebar-item
          :link="{name: 'Gerenciar Alertas', icon: 'ni ni-key-25 text-blue', path: '/alertas'}"
        />
      </template>
    </side-bar>
    <div class="main-content" :data="sidebarBackground">
      <dashboard-navbar></dashboard-navbar>

      <div @click="toggleSidebar">
        <fade-transition :duration="200" origin="center top" mode="out-in">
          <!-- your content here -->
          <router-view></router-view>
        </fade-transition>
        <content-footer v-if="!$route.meta.hideFooter"></content-footer>
      </div>
    </div>
  </div>
</template>
<script>
import DashboardNavbar from "./DashboardNavbar.vue";
import ContentFooter from "./ContentFooter.vue";
import { FadeTransition } from "vue2-transitions";

export default {
  components: {
    DashboardNavbar,
    ContentFooter,
    FadeTransition
  },
  data() {
    return {
      sidebarBackground: "vue" //vue|blue|orange|green|red|primary
    };
  },
  methods: {
    toggleSidebar() {
      if (this.$sidebar.showSidebar) {
        this.$sidebar.displaySidebar(false);
      }
    }
  }
};
</script>
<style lang="scss">
</style>
