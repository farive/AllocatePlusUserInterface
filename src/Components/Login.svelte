<script>

    import {createEventDispatcher} from "svelte";

    let dispatch = createEventDispatcher();
    let username;
    let password;
    let authenticate;

    const handleSubmit = () => {
        const loginInfo = {
            username: username,
            password: password,
            authenticate: authenticate
        }
        dispatch("handleLoginInfo", loginInfo);
    }
</script>

<form on:submit|preventDefault={handleSubmit}>
    <h1>Login</h1>
    <div class = "group">
        <input type = "text" placeholder="Username" bind:value={username}>
    </div>

    <div class = "group">
        <input type = "text" placeholder="Password" bind:value={password}>
    </div>

    <div class = "group">
        <input type = "text" placeholder = "Authenticate Key" bind:value={authenticate}>
    </div>
    <button>Login</button>
</form>

<style>
    form {
        display: flex;
        flex-direction: column;
        align-items: center;
        border: 1px black solid;
        padding: 10px;
        width: fit-content;
    }

    input {
        border: 0px none;
        margin: 10px;
        width: fit-content;
    }
</style>