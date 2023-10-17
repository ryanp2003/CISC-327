<script>
    let username = ""
    let password = ""

    const login = () => {
        return
    }

</script>

<div class="flex flex-col bg-gray-600 grow p-5 text-center w-[100vw] h-[100vh]">
    <div class="text-8xl font-bold text-transparent bg-clip-text bg-gradient-to-b from-yellow-500 to-orange-500 p-5 overscroll-none">
        Log In
    </div>
    <div class="flex flex-col text-left text-white font-bold py-10 text-left justify-center mx-auto">
        <div class="text-4xl pb-2">Username</div>
        <input bind:value={username} type="text" class="w-full text-black text-2xl p-1 rounded-md">
        <div class="text-4xl pb-2 pt-10">Password</div>
        <input bind:value={password} type="text" class="w-full text-black text-2xl p-1 rounded-md">
    </div>
    <button on:click={login} class="mx-auto p-5 rounded-md text-4xl text-white font-bold bg-gradient-to-b from-yellow-500 to-orange-500">
        Log In
    </button>
</div>
