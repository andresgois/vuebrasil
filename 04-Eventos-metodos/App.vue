<template>
	<div>
		<h1>Lista de tarefas</h1>
		<button @click="() => { showList = !showList}">
			Mostrar lista
		</button>
		<br>
		<input 
			@keyup.enter="addTask()" 
			type="text" 
			v-estaLa 
			v-model="currentTask">
		<br>
		<ul v-if="showList">
			<li
				v-for="task in tasks"
				@dblclick="complete(task)"
				:key="task"
				class="task-item"
				:class="{
					'line-through': task.isDone
				}"
			>{{ task.name }}    
			<button @click="remove(task)">&times;</button>
			</li>
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
			currentTask: '',
			showList: false,
			tasks: [
				{ name: 'Fazer curso', isDone: false }
			]
		}),
		methods: {
			addTask(){
				this.tasks.push({
					name: this.currentTask,
					isDone: false
				})
				this.currentTask = ''
			},
			complete(task){
				this.tasks = this.tasks.map(t => {
					if(t.name === task.name){
						return { ...t, isDone: !t.isDone }
					}
					return { ...t }
				})
			},
			remove(task){
				this.tasks = this.tasks.filter(t => t.name !== task.name)
				console.log(task);
			}
		}
	}
</script>


<style scoped>
	.line-through{
		text-decoration: line-through;
	}
	.task-item{
		cursor: pointer;
	}
</style>