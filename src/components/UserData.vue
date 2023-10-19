<template>
	<form @submit.prevent="submitData">
		<label for="name">Name:</label>
		<input type="text" v-model="enteredName" />
		<label for="name">Age:</label>
		<input type="text" v-model="enteredAge" />
		<button>Submit</button>
	</form>
</template>

<script>
export default {
	emits: ['add-user-details'],
	data() {
		return {
			enteredName: '',
			enteredAge: '',
		};
	},
	methods: {
		submitData() {
			this.$emit('add-user-details', this.enteredName, this.enteredAge);
			this.enteredName = '';
			this.enteredAge = '';
		},
	},
};
</script>
