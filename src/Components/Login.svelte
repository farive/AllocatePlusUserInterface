<script>
    let username;
    let password;
    let authenticate;

    const btnClick = () => {
        console.log("potato");
    }
</script>

<form>
    <div class = "group">
        <label for="username">Enter your user name here</label>
        <input type = "text" bind:value={username}>
    </div>

    <div class = "group">
        <label for="password">Enter your password here</label>
        <input type = "text" bind:value={password}>
    </div>

    <div class = "group">
        <label for = "authenticate">Enter your authenticate key here</label>
        <input type = "text" bind:value={authenticate}>
    </div>
</form>

<style>
    .group {
        display: flex;
        margin-bottom: 10px;
    }
    label {
        float: left;
        display: block;
    }
</style>