<script lang="ts">
    let username: string
    let password: string

    async function login(){

    }
</script>

<div class='h-full flex justify-center items-center'>
    <div class='flex flex-col rounded-md border border-gray-400 bg-gray-100 shadow-lg p-8 xl:w-1/4 lg:w-1/3 w-full m-4'>
        <span class='text-5xl font-mono pb-6 self-center'>Log in :3</span>

        <label for="username" class='py-2'>Username</label> 
        <input type="text" bind:value={username} class='field'/>

        <label for="password" class='py-2'>Password</label> 
        <input type="password" bind:value={password} class='field'/>

        <button class='btn-primary-full my-6' on:click={login}>Login</button>
        <hr class='border-t-2 border-gray-400 mb-3'/>
        <span class='text-2xl self-center'>Don't own an account?</span>
        <a href="/register" class='btn-primary mt-3'>Register</a>
    </div>
</div>

