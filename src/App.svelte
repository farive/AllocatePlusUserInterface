<script lang="ts">
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
	<div class = "Login">
		<Login on:handleLoginInfo={handleLoginInfo}/>
	</div>
</main>

<style>
	.Login{
		display: flex;
		justify-content: left;
	}
</style>