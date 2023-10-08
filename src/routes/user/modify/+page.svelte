<script lang="ts">
    interface UserData {
        username: string,
        email: string
        coins: number
    }
    let user: UserData = {
        username: "matbmp",
        email: "matbmp@gmail.com",
        coins: 100000000
    }
</script>

<div class="h-full flex items-center justify-center">
    <div class='flex flex-col rounded-md border border-gray-400 bg-gray-100 shadow-lg p-8 xl:w-1/4 lg:w-1/3 w-full m-4'>
        
        <label for="email" class='py-2'>Email</label> 
        <input type="email" bind:value={user.email} class='field'/>

        <label for="username" class='py-2'>Username</label> 
        <input type="text" bind:value={user.username} class='field'/>

        <a href="/register" class='btn-primary-full mt-6'>Save changes</a>
    </div>
</div>