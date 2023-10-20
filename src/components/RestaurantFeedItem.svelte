<script>
    export let category;
    export let name;
    export let image;
    export let price;

</script>

<a href="/generic_menu">
    <div class="p-3 text-center font-bold text-white rounded-md flex flex-col items-center bg-[#888098] duration-[1s]">
        <div class="text-xl text-[#344055]">{name}</div>
        <img src={image} alt="Not available" class="z-0 h-[12vh] opacity-80 rounded-md scale-[0.8]">
        <div class="text-xl text-[#344055]">{price}</div>
    
    </div>
</a>