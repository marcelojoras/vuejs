<template>
    <div>
        <button @click="primeiro('Primeiro evento', $event), segundo('Segundo evento', $event)">Ativar mĂșltiplos eventos</button>
        <p>{{multiplos_eventos}}</p>
    </div>
</template>

<script>
    export default {
        name: 'MultiplosEventos',
        data() {
            return {
                multiplos_eventos: ''
            }
        },
        methods: {
            primeiro(txt, e) {
                this.multiplos_eventos = txt
            },
            segundo(txt, e) {
                setTimeout(() => {
                    this.multiplos_eventos = txt
                }, 500);
            }
        }
    }
</script>

<style scoped>
    div {
        margin: 100px;
    }
</style>