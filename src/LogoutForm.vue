<template>
   <div>
      	 <label>Wyloguj sie {{ username }}</label>
      	 <button @click="$emit('logout')">Wyloguj</button>
      	 <h2>Spotkania</h2>
      	 <button @click="addNewMeeting()">Dodaj spotknie</button>
      	 <label>{{ meetings }}</label>
      	 <ol>
 	   		<li v-for="item in meetings" :key="item.id">{{ item }}</li>
		</ol>
   </div>
</template>

<script>
export default {
	props: ['username'],
	data(){
		return {
			meetings: [
				'MOW',
				'TO',
				'MIS'
			]
		};
	},
	methods: {
    	addNewMeeting() {
       		this.meetings.push('nowe');
   	 	}
}
}
</script>