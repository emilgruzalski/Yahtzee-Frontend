<script lang="ts">

    let password: string = ""
    let confirmPassword: string = ""
</script>

<div class="h-full flex items-center justify-center">
    <div class='flex flex-col rounded-md border border-gray-400 bg-gray-100 shadow-lg p-8 xl:w-1/4 lg:w-1/3 w-full m-4'>

        <label for="password" class='py-2'>Password</label> 
        <input type="password" bind:value={password} class='field'/>

        <label for="password" class='py-2'>Confirm password</label> 
        <input type="password" bind:value={confirmPassword} class='field'/>

        <a href="/register" class='btn-primary-full mt-6'>Save changes</a>
        <a href="/register" class='btn-primary mt-6'>Back</a>
    </div>
</div>