<script>
    export let category;
    export let name;
    export let image;
    export let price;

</script>

<div class="p-1 text-center font-bold text-white rounded-md flex flex-col items-center bg-[#888098]">
     <div class="text-xl text-[#344055]">{name}</div>
     <img src={image} alt="Not available" class="z-0 h-[12vh] opacity-80 rounded-md scale-[0.8]">
     <div class="text-xl text-[#344055]">{price}</div>
</div>