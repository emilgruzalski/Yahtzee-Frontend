<script lang="ts">
    let username: string
    let password: string

    async function login(){

    }
</script>

<div class='h-full flex justify-center items-center'>
    <div class='flex flex-col rounded-md border border-gray-400 bg-gray-100 shadow-lg p-8 xl:w-1/4 lg:w-1/3 w-full m-4'>
        <span class='text-5xl font-mono pb-6 self-center'>Logowanie :3</span>

        <label for="username" class='py-2'>Nazwa użytkownika</label> 
        <input type="text" bind:value={username} class='field'/>

        <label for="password" class='py-2'>Hasło</label> 
        <input type="password" bind:value={password} class='field'/>

        <button class='bg-blue-700 hover:bg-blue-700/80 text-white rounded-md my-6 p-3' on:click={login}>Login</button>
        <hr class='border-t-2 border-gray-400 mb-3'/>
        <span class='text-2xl self-center'>Nie masz konta?</span>
        <a href="/register" class='border-2 border-blue-400 bg-blue-100 hover:bg-blue-200 text-black rounded-md mt-3 p-3 text-center'>Rejestracja</a>
    </div>
</div>

<style lang='postcss'>
    .field{
        @apply border-2 border-gray-300 focus:outline-gray-400 rounded-md p-2
    }
</style>