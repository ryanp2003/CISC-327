<script>
    import RestaurantFeedItem from "./RestaurantFeedItem.svelte";
    export let category;
    export let price;
    export let nameFilter;

    let c = 0;
    let restaurantFeeds = [];
    // Here we would send an http request to backend to properly fill this category
    //
    //
    //

    // But for the front-end prototype:
    for (let i=0; i < 10; i++) {
        let newRestaurantFeedItem = {category: category, nameID: i};
        // newRestaurantFeedItem.category = category;
        // newRestaurantFeedItem.name = i;
        if (i < 3) {
            newRestaurantFeedItem.price = "$";
        }
        else if (i < 7) {
            newRestaurantFeedItem.price = "$$";
        }
        else {
            newRestaurantFeedItem.price = "$$$";
        }
         restaurantFeeds.push(newRestaurantFeedItem);
    }
</script>
<div class="w-[100vw] bg-[#CFB3CD] border-t-[2rem] border-[#344055] py-4 px-3 overflow-none">
    <div class="text-3xl text-[#344055] pb-4 font-bold">{category}</div>
    <div class="flex flex-row gap-10 justify-spread group relative px-20 overflow-scroll overflow-y-hidden">
        <!-- <button class="w-16 bg-[#888098] text-4xl px-4 rounded-md absolute left-0 h-full z-10 opacity-80"> ⇦ </button> -->
        {#each restaurantFeeds as item}
            {#if (price == "Any" || item.price == price)}  
            <RestaurantFeedItem category={item.category} price={item.price} name="{item.category}_{item.nameID}" image="https://picsum.photos/300"></RestaurantFeedItem>
            {/if}
        {/each}
        <!-- <button class="w-16 bg-[#888098] text-4xl absolute right-0 h-full opacity-80 hover:text-white"> ⇨ </button> -->
    </div>
</div>      

