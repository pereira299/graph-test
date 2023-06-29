<template>
  <div>
    <StyledHeader></StyledHeader>
    <div class="d-flex flex-row bg-body-tertiary col-12 wrapper">
      <Sidebar></Sidebar>
      <main class="col-10 p-3">
        <slot></slot>
      </main>
    </div>
  </div>
</template>

<script>
import StyledHeader from '~/components/Header'
import Sidebar from '~/components/Sidebar'
export default {
  name: 'Layout',
  components: {
    StyledHeader,
    Sidebar,
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
}
</script>

<style>
main {
    background: #e9e9e9;
}

.wrapper {
    margin-top: 4.5rem;
}
</style>
