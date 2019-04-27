<template>
<!--  MDN web docs  -->
 	<div id="app">
    	<h1>{{logged}} Witaj w systemie do zapisów na zajęcia</h1>

    	<div v-if="logged == false">
    		<p>Zaloguj się e-mailem: 
			<input type="text" v-model="email">
			<button @click = "loginWithEmail()"> Zaloguj się </button>	
			</p>	
		</div>
		<div v-else>
			<p>Witaj {{email}}</p>
			<button @click = "logOutWithEmail()"> Wyloguj sie </button>
		</div>
    	
    	<!--<input type="text" v-model="email">
    	<button @click = "alertMyEmail()">Zaloguj sie</button>
    	
    	<div v-if="email.length < 10">Ale masz krótki adres!</div>
		<div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
		<div v-else>Twój adres e-mail jest stanowczo za długi.</div>-->
  	</div>
</template>


<script>
import "milligram";

export default {
	data() {
		return {
			email: 'TwojaStaraToTwojStary',
			password: '',
			logged: false
		};
	},
	methods: {
		alertMyEmail() {
		    alert(this.email);
		},
		loginWithEmail() {
			this.logged = true;
		},
		logOutWithEmail() {
			this.email = '';
			this.logged = false;
		}
	}
}
</script>


<style>
/* komentarz */	
</style>
