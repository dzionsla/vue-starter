<template>
   <div>
       <label>Wyloguj sie {{ username }}</label>
       <button @click="$emit('logout')">Wyloguj</button>
   </div>
</template>

<script>
export default {
	props: ['username'],
}
</script>