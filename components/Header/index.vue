<template>
  <header
    class="col-12 px-2 py-2 shadow d-flex flex-row"
  >
    <div class="col-1 col-sm-4 col-md-3 col-xl-2" @click="openDrawer">
        <i class="fa-solid fa-bars fa-3xl text-body-tertiary d-md-none"></i>
    </div>
    <div class="">
      <figure class="mb-0">
        <img src="/logo.png" alt="Logo" class="col-2" />
      </figure>
    </div>
    <div
      class="d-md-flex flex-row xs-hidden col-sm-4 col-md-3 col-xl-2 justify-content-between"
    >
      <i class="fa-solid fa-database fs-5 my-auto text-body-tertiary"></i>
      <i
        class="fa-solid fa-table-cells-large fs-5 my-auto text-body-tertiary"
      ></i>
      <i class="fa-solid fa-expand fs-5 my-auto text-body-tertiary"></i>
      <p class="my-auto">{{ username }}</p>
      <img src="/avatar.png" alt="Avatar" class="rounded-circle avatar" />
    </div>
    <div class="col-1 col-sm-4 d-md-none"></div>
  </header>
</template>

<script>
export default {
  name: 'StyledHeader',
  data() {
    return {
      username: 'John Doe',
    }
  },
  methods: {
    openDrawer() {
        console.log('open drawer')
      this.$emit('open-drawer')
    },
  },
}
</script>

<style scoped>
@media screen and (max-width: 768px) {
  .xs-hidden {
    display: none;
  }
}

@media screen and (max-width: 768px) {
  header {
    justify-content: center;
  }
}

.fa-3xl {
    font-size: 3rem;
    color: #2a82a9;
}

header {
  position: fixed;
  top: 0;
  z-index: 5;
  justify-content: space-between;
}
header,
header * {
  height: auto;
  background: #fff;
}

header img {
  height: 3.5rem;
  width: 100%;
  object-fit: contain;
}

.avatar {
  height: 3rem;
  width: 3.5rem;
  background: '#c2c2c2';
  object-fit: contain;
  border-radius: 50%;
}
</style>
