<template>
  <header class="col-12 px-2 py-2 shadow justify-content-between d-flex flex-row">
    <div class="col-2"></div>
    <div>
        <figure class="mb-0">
            <img src="/logo.png" alt="Logo" class="col-2">
        </figure>
    </div>
    <div class="d-flex flex-row col-2 justify-content-between">
        <i class="fa-solid fa-database fs-5 my-auto text-body-tertiary"></i>
        <i class="fa-solid fa-table-cells-large fs-5 my-auto text-body-tertiary"></i>
        <i class="fa-solid fa-expand fs-5 my-auto text-body-tertiary"></i>
        <p class="my-auto">{{username}}</p>
        <img src="/avatar.png" alt="Avatar" class="rounded-circle avatar">

    </div>
  </header>
</template>

<script>

export default {
    name: 'StyledHeader',
    data() {
        return {
            username: 'John Doe'
        }
    }
}
</script>

<style scoped>
header {
    position: fixed;
    top: 0;
}
header, header * {
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
    background: "#c2c2c2";
    object-fit: contain;
    border-radius: 50%;
}
</style>