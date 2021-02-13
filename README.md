# VUE

## vue serve
## npm run serve

A versão mais recente do Sublime corrigiu esse problema, clique em Preferências, clique em Tema, selecione Adaptive.sublime-theme . Isso mudará a barra lateral para um fundo de cor escura.

### Binding
- v-bind:style="{color: color1}"
- ou 
- :style="{color}" // se nome chave e valor são iguais

- v-on:keyup  || v-on:click="" ... @click=""
- @keyup.enter="addFood"
- no form | @submit.prevent=""

## Inicio
- Página Oficial: https://vuejs.org/
- Formas de usar o Vue
	- CDN: <script src="https://cdn.jsdelivr.net/npm/vue@2/dist/vue.js"></script>
	- <script src="https://cdn.jsdelivr.net/npm/vue@2"></script>
- Plugins
	- Vue
	- Vetur

##### Sigle file components
- npm install -g @vue/cli @vue/cli-service-global
- vue serve
- http://localhost:8080/

##### 02 - Data binding
- two way data binding
- v-bind:style="color"
- data: () => ({ color: 'green' })
- ou   :style="color"

##### 03 - Diretivas
- v-if
- v-else
- v-for
- cria novas diretivas, tem que esta dentro do export default
	- directives: {			estaLa: focus		}
	- <input type="text" v-estaLa>


##### v2
- options API

##### v3
- composition API
- Instant Prototyping não disponível

##### Life cycle hooks
- https://v3.vuejs.org/guide/composition-api-lifecycle-hooks.html#lifecycle-hooks
- 


