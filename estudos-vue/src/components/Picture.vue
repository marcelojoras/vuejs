<template>
    <div>
        <img :src="avatar" :alt="descricao"/>
        <MudarImagem @mudar-imagem="trocarImagem"/>
    </div>
</template>

<script>
    import MudarImagem from './MudarImagem.vue'
    export default {
        name: 'Picture',
        data() {
            return {
                avatar: '/img/avatar.jpg',
                descricao: 'Anya'
            }
        },
        components: {
            MudarImagem
        },
        methods: {
            trocarImagem() {
                this.avatar = '/img/avatar2.jpg'
            }
        }
    }
</script>