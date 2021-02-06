<template>
	<div>
		<h1>Lista de tarefas</h1>
		<button @click="() => { showList = !showList}">
			Mostrar lista
		</button>
		<br>
		<input type="text" v-estaLa>
		<br>
		<ul v-if="showList">
			<li
				v-for="task in tasks"
				:key="task"
			>{{ task.name }}</li>
		</ul>
		<p v-else>Lista de tarefas escondidas</p>
	</div>
</template>


<script>
	const focus ={
		inserted: (el) => {
			el.focus()
		}
	}
	export default {
		directives: {
			estaLa: focus
		},
		data: () => ({
			showList: false,
			tasks: [
				{ name: 'Fazer curso', isDone: false }
			]
		})
	}
</script>


<style>
	
</style>