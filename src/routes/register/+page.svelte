<script lang="ts">
    let email: string
    let username: string
    let password: string

    async function register(){

    }
</script>

<div class='h-full flex justify-center items-center'>
    <div class='flex flex-col rounded-md border border-gray-400 bg-gray-100 shadow-lg p-8 xl:w-1/4 lg:w-1/3 w-full m-4'>
        <span class='text-5xl font-mono pb-6 self-center'>Register :3</span>
        
        <label for="email" class='py-2'>Email</label> 
        <input type="email" bind:value={email} class='field'/>

        <label for="username" class='py-2'>Username</label> 
        <input type="text" bind:value={username} class='field'/>

        <label for="password" class='py-2'>Password</label> 
        <input type="password" bind:value={password} class='field'/>

        <button class='bg-blue-700 hover:bg-blue-700/80 text-white rounded-md mt-6 p-3' on:click={register}>Register</button>
    </div>
</div>
