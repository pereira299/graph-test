<template>
  <aside
    class="col-2 px-2 py-4 justify-content-between d-md-flex flex-column d-none"
  >
    <nav>
      <ul class="px-1">
        <li
          v-for="link in links"
          :key="link.text"
          class=""
        >
          <a :href="link.link" class="d-flex flex-row mb-2 justify-content-between text-decoration-none">
            <i
              :class="
                link.icon +
                ' fs-5 my-auto text-light py-2 col-3 rounded text-center mr-2'
              "
            ></i>
            <p class="my-auto col-8 text-dark">{{ link.text }}</p>
          </a>
        </li>
      </ul>
    </nav>
  </aside>
</template>

<script>
export default {
  name: 'Sidebar',
  data() {
    return {
      links: [
        {
          icon: 'fa-solid fa-book',
          text: 'Dashboard',
          link: '#',
        },
        {
          icon: 'fa-solid fa-user-plus',
          text: 'Clientes potenciais',
          link: '#leads',
        },
        {
          icon: 'fa-solid fa-briefcase',
          text: 'Negocios',
          link: '#business',
        },
      ],
    }
  },
}
</script>

<style scoped>
aside {
  height: calc(100vh - 4.5rem);
  background: #fff;
  position: fixed;
}

aside i {
  background: #2a82a9;
}
</style>
