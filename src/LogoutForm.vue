<template>
   	<div>
      	<label>Wyloguj sie {{ username }}</label>
      	<button @click="$emit('logout')">Wyloguj</button><br><br>
      	<!--  <h2>Zajęcia</h2>
      	<h4>Dodaj nowe spotkanie</h4>
      	<p>Nazwa</p>
      	<input type="text" v-model=name>
      	<p>Opis</p>
      	<textarea rows="2" cols="10"  v-model=description></textarea>
      	<button @click="addNewMeeting()">Dodaj spotknie</button>
      	
		<div v-if="meetings.length > 0">
    		 <table style="width:100%">
			  	<tr>
			    	<th>Nazwa spotkania</th>
			    	<th>Opis spotkania</th>
			  	</tr>
		        <tbody>
		            <tr v-for="meeting in meetings" :key="meeting.name">
		                <td>{{ meeting.name }}</td>
		                <td>{{ meeting.description }}</td>
		            </tr>
       		 	</tbody>
			</table> 
		</div> -->
		
	</div>
</template>

<script>
export default {
	props: ['username'],
	data(){
		return {
			meetings: [
				{"name": "MIT", "description": "opis tutaj dla MIT"},
				{"name": "EST", "description": "opis tutaj dla EST"}
			],
			name: '',
			description: ''
		};
	},
	methods: {
    	addNewMeeting() {
       		this.meetings.push({name: this.name, description: this.description});
   	 	}
	}
}
</script>