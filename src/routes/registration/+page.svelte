<script>
    let email = ""
    let username = ""
    let password = ""

    const register = () => {
        return
    }
    const signIn = () => {
        // window.location.href = 'http://localhost:5173';
        return
    }

</script>

<div class="flex flex-col bg-gray-600 grow p-5 text-center w-[100vw] h-[100vh]">
    <div class="text-8xl font-bold text-transparent bg-clip-text bg-gradient-to-b from-yellow-500 to-orange-500 p-5 overscroll-none">
        Create Account
    </div>
    <div class="flex flex-col text-left text-white font-bold py-10 text-left justify-center mx-auto">
        <div class="text-4xl pb-2">Email</div>
        <input bind:value={email} type="text" class="w-full text-black text-2xl p-1 rounded-md">
        <div class="text-4xl pb-2">Username</div>
        <input bind:value={username} type="text" class="w-full text-black text-2xl p-1 rounded-md">
        <div class="text-4xl pb-2">Password</div>
        <input bind:value={password} type="text" class="w-full text-black text-2xl p-1 rounded-md">
    </div>
    <div class="flex justify-center">
        <button on:click={register} class="p-5 rounded-md text-4xl text-white font-bold bg-gradient-to-b from-yellow-500 to-orange-500 hover:from-orange-500 hover:to-yellow-500 active:scale-[0.97]" style="margin-right: 5px">
            Register
        </button>
        <a href="/"><button on:click={signIn} class="p-5 rounded-md text-4xl text-white font-bold bg-gradient-to-b from-yellow-500 to-orange-500 hover:from-orange-500 hover:to-yellow-500 active:scale-[0.97]" style="margin-left: 10px">
            Sign-In
        </button>
        </a>
    </div>
</div>
