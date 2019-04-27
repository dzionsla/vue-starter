<template>
<!--  MDN web docs  -->
 	<div id="app">
    	<h1>{{logged}} Witaj w systemie do zapisów na zajęcia</h1>
    	<p> 
    	

    	<div v-if="logged == false">
    		<p>Zaloguj się e-mailem: </p>
			<input type="text" v-model="email">
			<button @click = "loginWithEmail()"> Zaloguj się </button>
		
		</div>
		<div v-else-if="logged == true">
			<p>Witaj {{email}}</p>
			<button @click = "logOutWithEmail()"> Wyloguj sie </button>
		</div>
    	</p>
    	
    	<!--<input type="text" v-model="email">
    	<button @click = "alertMyEmail()">Zaloguj sie</button>
    	
    	<div v-if="email.length < 10">Ale masz krótki adres!</div>
		<div v-else-if="email.length < 15">Twój adres e-mail jest w sam raz.</div>
		<div v-else>Twój adres e-mail jest stanowczo za długi.</div>-->
  	</div>
</template>


<script>
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
			this.logged = false;
		}
	}
}
</script>


<style>
/* komentarz */	
</style>
