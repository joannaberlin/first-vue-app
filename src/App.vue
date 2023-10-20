<template>
	<section>
		<header>Hey there</header>
	</section>
	<active-user :user-name="user.name" :user-age="user.age"></active-user>
	<user-data @add-user-details="addUserDetails"></user-data>
</template>

<script>
import UserData from './components/UserData.vue';
export default {
	components: { UserData },
	data() {
		return {
			user: {
				name: 'John',
				age: 0,
			},
		};
	},
	methods: {
		addUserDetails(userName, userAge) {
			const user = {
				name: userName,
				age: +userAge,
			};
			this.user = user;
		},
	},
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Jost&display=swap');
* {
	box-sizing: border-box;
}

html {
	font-family: 'Jost', sans-serif;
}

body {
	margin: 0;
	background-color: #ded4ca;
}

header {
	box-shadow: 0 2px 8px rgba(8, 8, 8, 0.26);
	margin: 3rem auto;
	border-radius: 10px;
	padding: 1rem;
	background-color: #5a5349;
	color: white;
	text-align: center;
	width: 90%;
	max-width: 40rem;
}

#app button {
	font: inherit;
	cursor: pointer;
	border: 1px solid #fe723f;
	background-color: #fe723f;
	border-radius: 5px;
	color: white;
	padding: 0.05rem 1rem;
	margin: 1rem 0;
	box-shadow: 1px 1px 2px rgba(0, 0, 0, 0.26);
	max-width: 10rem;
}

#app h2,
h3 {
	font-size: 1.5rem;
	border-bottom: 4px solid #cccccc;
	color: #fe723f;
	margin: 0 0 1rem 0;
}

#app div {
	width: 90%;
	max-width: 40rem;
	margin: auto;
}

#app form {
	box-shadow: 0 2px 8px rgba(0, 0, 0, 0.26);
	margin: 1rem auto;
	border-radius: 10px;
	padding: 1rem;
	text-align: center;
	width: 90%;
	max-width: 40rem;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	max-width: 20rem;
}
</style>
