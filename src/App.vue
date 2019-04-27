<template>
 	<div id="app">
    	<h1>Witaj w systemie do zapisów na zajęcia</h1>

    	<div v-if="email.length == 0">
    		<form @submit.prevent="">
    			<!--<p>Zaloguj się e-mailem: 
				<input type="text" v-model="email">
				<button @click = "loginWithEmail($event)"> Zaloguj się </button>	
								<login-form @login="loginWithEmail($event)" 
							button-label="Rejestruję się"
							header="Rejestracja"></login-form>
				</p> -->

				<login-form @login="loginWithEmail($event)" 
							button-label="Loguję się"
							header="logowanie"></login-form>
			</form>	
		</div>
		
		<div v-else>
			<logout-form :username='email'
						 @logout="logOutWithEmail()"> 
			</logout-form>
			<meeting-page>
			</meeting-page>
			<!-- <p>Witaj {{email}}</p>
			<button @click = "logOutWithEmail()"> Wyloguj sie </button> -->
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
import LoginForm from "./LoginForm";
import LogoutForm from "./LogoutForm";
import MeetingPage from "./MeetingPage";

export default {
	components: {LoginForm, LogoutForm, MeetingPage},
	data() {
		return {
			email: 'TwojaStaraToTwojStary',
			password: '',
		};
	},
	methods: {
		alertMyEmail() {
		    alert(this.email);
		},
		loginWithEmail(username) {
			this.email = username;
		},
		logOutWithEmail() {
			this.email = '';
		}
	}
}
</script>


<style>
/* komentarz */	
</style>
