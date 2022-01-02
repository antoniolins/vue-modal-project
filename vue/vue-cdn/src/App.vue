/* eslint-disable prettier/prettier */

<template>
	<h1>Hello Vue by Alins</h1>
	<div>{{ author }}</div>
</template>

<script>
	export default {
		name: 'App',

		data() {
			return {
				showBooks: true,
				title: 'The Way of Kings',
				author: 'Brandon Sanderson',
				age: 45,
			};
		},
		methods: {
			toggleShowBooks() {
				this.showBooks = !this.showBooks;
			},
		},
	};
</script>

<style>
	#app {
		font-family: Avenir, Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		text-align: center;
		color: #2c3e50;
		margin-top: 60px;
	}
</style>
