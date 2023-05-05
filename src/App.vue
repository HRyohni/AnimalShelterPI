<template>
	<v-app>
		<v-app-bar app color="yellow" 
		
		style="text-align: right; color: white;">
		<h1 style="text-shadow: 2px 2px #000000;">AS</h1>
			<v-spacer></v-spacer>
			
			<v-btn v-show="isAuthenticated" text to="/animal" style="text-align: right; ">New Animal</v-btn>
			<v-btn v-show="false && isAuthenticated" text to="/profile">
				Profile
			</v-btn>
			<v-btn v-show="!isAuthenticated" text to="/login">Login</v-btn>
			<v-btn v-show="!isAuthenticated" text to="/registration">
				Registration
			</v-btn>
			<v-btn v-show="isAuthenticated" @click="signOut" text>Logout</v-btn>

			<v-spacer></v-spacer>
		</v-app-bar>

		<v-main>
			<router-view />
		</v-main>
		<bottomBar></bottomBar>
	</v-app>
</template>

<script>
import { auth, getAuth, onAuthStateChanged, signOut } from "../firebase.js";
import bottomBar from '@/components/bottomBarView.vue';
export default {
	name: "App",
	data() {
		return {
			isAuthenticated: false,
			isAuthorized: false,
			email: null,
			showRequest: false,
			showAdd: false,
		};
	},
	methods: {
		signOut() {
			const auth = getAuth();
			signOut(auth)
				.then(() => {
					console.log("signed out");
				})
				.catch((error) => {
					// An error happened.
				});
		},
	},
	beforeCreate() {59+
		onAuthStateChanged(auth, (user) => {
			if (user) {
				console.log("Authenticated");
				this.isAuthenticated = true;
			} else {
				console.log("Not Authenticated");
				this.isAuthenticated = false;
			}
		});
	},
	components:
    {
        bottomBar
    },
};
</script>
<style scoped></style>
