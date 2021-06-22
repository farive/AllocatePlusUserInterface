<script lang="ts">
	import Calendar from "./Components/Calendar.svelte";
import Login from "./Components/Login.svelte"

	let loginInfo = {
		username: "",
		password: "",
		authenticate: 0
	}

	const handleLoginInfo = (event) => {
		loginInfo["username"] = event.detail["username"];
		loginInfo["password"] = event.detail["password"];
		loginInfo["authenticate"] = event.detail["authenticate"];
	}
</script>

<main>
	<Login on:handleLoginInfo={handleLoginInfo}/>
	<Calendar/>
</main>

<style>
	main{
		display: flex;
		flex-direction: row;
		gap: 12px;
		margin: 5px;
	}
</style>