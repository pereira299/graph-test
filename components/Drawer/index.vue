<template>
    <dialog :open="open">
        <i class="fa-solid fa-xmark text-brand col-auto text-right" @click="closeDrawer"></i>
        <div class="d-flex flex-row">
            <img src="/avatar.png" alt="Avatar" class="rounded-circle avatar col-4" />
            <p class="my-auto fs-3 col-8">{{ username }}</p>
        </div>
        <hr class="col-12 border-bottom border-secondary"/>
        <nav class="col-12">
            <ul class="px-1 list-group col-12">
                <li
                    v-for="link in links"
                    :key="link.text"
                    class="list-group-item"
                >
                    <a :href="link.link" class="d-flex flex-row mb-2 col-12 mx-auto justify-content-center text-decoration-none">
                        <p class="my-auto col-8 text-dark fs-4 text-center">{{ link.text }}</p>
                    </a>
                </li>
            </ul>
        </nav>
    </dialog>
</template>

<script>
export default {
    name: 'Drawer',
    props: {
        open: {
            type: Boolean,
            default: true,
        },
    },
    data() {
        return {
            username: 'John Doe',
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
    methods: {
        closeDrawer() {
            this.$emit('close')
        },
    },
}
</script>

<style scoped>
.text-brand {
    color: #2a82a9;
}

dialog {
    width: 100vw;
    height: 100vh;
    background: #fff;
    position: fixed;
    padding: 1rem;
    top: 0;
    left: 0;
    z-index: 50;
}

.avatar {
  height: auto;
  width: 9rem;
  background: '#c2c2c2';
  object-fit: contain;
  border-radius: 50%;
}

dialog > i {
    margin-left: calc(100vw - 5rem);
    font-size: 4rem;
}
</style>