<template>
	<div>
		<h1
			:style="{color}"
		>Hello {{name}}</h1>
		<input type="text" v-model="name">
	</div>
</template>


<script>
	export default {
		data: () => ({
			name : 'André Gois',
			color: 'tomato'
		})
	}
</script>


<style>
	
</style>