<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
        <p v-else>Estou em busca de novas oportunidades</p>
        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
            <li v-for="(tech, index) in backendTechs" v-bind:key="index">
                {{tech}}
            </li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end</p>
        <ul>
            <li v-for="tech in frontendTechs" v-bind:key="tech.id">
                {{tech.language}}
            </li>
        </ul>
        <div>
            <button @click="showEmail">{{texto_botao}}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para {{email}}</p>
        <p class="teste">Para acessar meu portifólio <a v-bind:href="meu_link">basta clicar aqui</a></p>
        <Picture/>
    </div>
</template>

<script>
    import Picture from './Picture.vue'
    export default {
        name: 'Info',
        props: {
            email: String,
            esta_trabalhando: Boolean
        },
        data() {
            return {
                mostrar_email: false,
                meu_link: 'https://google.com.br',
                texto_botao: 'Mostrar E-mail',
                backendTechs: [
                    'Javascript',
                    'PHP',
                    'Phyton'
                ],
                frontendTechs: [
                    {
                        id: 1,
                        language: 'HTML'
                    },
                    {
                        id: 2,
                        language: 'CSS'
                    },
                    {
                        id: 3,
                        language: 'Vue'
                    }
                ]
            }
        },
        components: {
            Picture
        },
        methods: {
            showEmail() {
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email) {
                    this.texto_botao = 'Motrar E-mail'
                } else {
                    this.texto_botao = 'Esconder E-mail'
                }
            }
        }
    }
</script>

<style>
    .paragrafo-pai {
        color: red;
    }
</style>