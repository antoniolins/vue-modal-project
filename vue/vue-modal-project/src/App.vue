<template>
	<h1>{{ title }}</h1>
	<div v-if="showModal">
		<div>Wellcome...</div>
		<Modal theme="sale" @close="toggleModal">
			<template v-slot:links>
				<a href="#">Sign up now </a>
				<a href="#"> More info... </a>
			</template>
			<h1>Ninja Givaway!</h1>
			<p>Grab your ninja swag for half price!</p>
		</Modal>
	</div>
	<button @click.alt="toggleModal">Open Modal (Alt)</button>
</template>

<script>
	import Modal from './components/Modal';

	export default {
		name: 'App',
		components: { Modal },
		data() {
			return {
				title: 'My First Vue App!',
				header: 'Sign up for the Giveaway ',
				text: 'Grab your ninja swag for half price!',
				showModal: true,
			};
		},
		methods: {
			toggleModal() {
				this.showModal = !this.showModal;
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
	h1 {
		border-bottom: 1px solid #ddd;
		display: inline-block;
		padding-bottom: 10px;
	}
</style>
