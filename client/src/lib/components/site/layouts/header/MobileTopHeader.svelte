<script>
import { fly } from 'svelte/transition';
import MenuIcon from './MenuIcon.svelte'

let Drawer=false;
function openDrawer(){
    return Drawer=!Drawer
}

</script>

<div class=" top-0 right-0 left-0 lg:hidden flex justify-between bg-green-200 shadow-md">
    <div class="m-1 z-50">
        <a  href="/">
            <div class="font-semibold text-xl">
                <span class=" text-gray-500 semibold">Каркас</span><span class="text-yellow-500">Центр</span>
            </div>
        </a >
    </div>
    <div class="flex">
        <a rel="external" href="https://wa.me/message/S2HVLZUQSNBBN1" >
            <i class="fa fa-whatsapp text-lg mt-1 text-gray-500 font-thin" aria-hidden="true"></i> 
        </a>
        <a rel="external" href="tel:+79308200225">
            <i class="fa fa-phone text-lg  ml-7 mt-1 text-gray-500 font-thin"></i> 
        </a>
    </div>
    <div class="z-50">
        <div on:click={openDrawer} class=" w-7 h-5 cursor-pointer  mt-2 mr-3">
            <MenuIcon />
        </div>
        
        <!-- <i class="fa fa-bars text-2xl mr-5 mt-1 text-gray-500" aria-hidden="true" on:click={openDrawer}></i> -->
    </div>

</div>

<!-- Боковое меню -->

{#if Drawer}
<aside transition:fly="{{ x: -100, duration: 500 }}" class="fixed  top-0 w-screen h-screen bg-green-50 z-40" >
    <div class="flex justify-end">
        <div >
            
            <!-- <i class="fa fa-times  text-4xl mr-5 mt-1 text-gray-500" aria-hidden="true" on:click="{openDrawer}"></i> -->
        </div>
        
    </div>
</aside>
{/if}
