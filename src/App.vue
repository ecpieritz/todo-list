<template>
	<div id="app">
		<h1>ToDo List</h1>
		<TaskGrid :tasks='tasks' />
	</div>
</template>

<script>
import TaskGrid from './components/TaskGrid.vue'

export default {
	components: {TaskGrid},
	data(){
		return {
			tasks:  [
				{name: 'Washing dirty dishes', pending: true}, 
				{name: 'Buying vegetables', pending: false}, 
				{name: 'Buy cat food', pending: false}, 
				{name: 'Clean the house', pending: false}, 
			]
		}
	}
}
</script>

<style>
	body {
		font-family: 'Lato', sans-serif;
		background: linear-gradient(to bottom, #023557, #4a84aa);
		color: #FFF;
	}

	#app {
		display: flex;
		flex: 1;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		height: 100vh;
	}

	#app h1 {
		margin-bottom: 5px;
		font-weight: 300;
		font-size: 3rem;
	}
</style>
