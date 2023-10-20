<script>
    export let cart;
    export let itemCount;
    export let className;

    let totalPrice = 0
    for (let i=0; i < cart.length; i++) {
        console.log(cart[0][i])
        totalPrice += cart[i].price;
    }
    console.log(totalPrice)

    

</script>


<div class={className}>
    <div class="text-3xl">Cart Items</div>
    <div class="flex flex-col text-left p-5 overflow-y-scroll text-white divide-y">
        {#each cart as item}
            <div class="flex flex-row">
                <div class="text-lg text-white"><b>{item.name}</b> • ${item.price}</div>
                <button class="ml-auto text-red-400" 
                on:click={() => { 
                    for (let i=0; i < cart.length; i++) {
                        if (cart[i].cartID=== item.cartID) {
                            cart.splice(i, 1)
                            itemCount = cart.length;
                            break;
                        }
                        // console.log()
                    }


                }}>Remove</button>
            </div>
        {/each}  
        <div class="">Sub-Total: ${Math.round(totalPrice * 100)/100}</div>
    </div>
</div>


<style>
    /* Hide scrollbar for Chrome, Safari and Opera */
.no-scrollbar::-webkit-scrollbar {
    display: none;
}

/* Hide scrollbar for IE, Edge and Firefox */
.no-scrollbar {
    -ms-overflow-style: none;  /* IE and Edge */
    scrollbar-width: none;  /* Firefox */
}

/* width */
::-webkit-scrollbar {
    width: 10px;
    height:10px;
}
 
/* Track */
::-webkit-scrollbar-track {
    background: transparent;
    border-radius: 5px;
}
 
/* Handle */
::-webkit-scrollbar-thumb {
    background: #344055;
    border-radius: 5px;
}
 
/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
    background: #555;
}
</style>