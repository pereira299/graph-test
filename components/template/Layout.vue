<template>
  <div>
    <StyledHeader @open-drawer="openDrawer"/>
    <div class="d-flex flex-row bg-body-tertiary col-12 wrapper">
      <Sidebar />
      <Drawer :open="drawerOpen" @close="drawerClose"/>
      <main class="col-12 col-md-10 p-3 offset-md-2">
        <slot></slot>
      </main>
    </div>
  </div>
</template>

<script>
import StyledHeader from '~/components/Header'
import Sidebar from '~/components/Sidebar'
import Drawer from '~/components/Drawer'
export default {
  name: 'Layout',
  components: {
    StyledHeader,
    Sidebar,
    Drawer,
  },
  head: {
    title: 'My App',
    link: [
      {
        rel: 'stylesheet',
        href: 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css',
      },
    ],
  },
  data() {
    return {
      drawerOpen: false,
    }
  },
  methods: {
    openDrawer() {
      console.log('open drawer 2')
      this.drawerOpen = true;
    },
    drawerClose() {
      this.drawerOpen = false;
    },
  },
}
</script>

<style>
main {
  background: #e9e9e9;
}

.wrapper {
  margin-top: 4.5rem;
}

/* width */
::-webkit-scrollbar {
  width: 10px;
}

/* Track */
::-webkit-scrollbar-track {
  background: #e9e9e9; 
}
 
/* Handle */
::-webkit-scrollbar-thumb {
  background: #2a82a9; 
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #33a4d4; 
}
</style>
