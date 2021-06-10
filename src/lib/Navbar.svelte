<script lang="ts">
import { onMount } from 'svelte';
    import NavbarElement from './NavbarElements.svelte';
    import { elasticOut } from 'svelte/easing';
import NavbarElements from './NavbarElements.svelte';

    let visible = false;
    function changeButton(){
        visible = !visible
    }
    function enlarge(node,{duration}){
        navbar.style.height = "5rem";
        return {
            duration,
            css: t => {
				const eased = elasticOut(t);
				return `
					transform: scale(${eased});
                    `
			}
        }
    }
    function dislarge(node,{duration}){
        return {
            duration,
            tick: t => {
                if(t == 0)
                    navbar.style.height = "";
            },
            css: t => {
				const eased = elasticOut(t);

				return `
					transform: scale(${eased});
                `
			}
        }
    }
    let navbar;
    onMount(()=>{
        navbar = document.getElementById('navbar');
    });
</script>
<style lang="sass" global>
    @import '../themes/Navbar.sass'
</style>
<nav id="navbar">
    <button on:click="{changeButton}">
        <i class="fas fa-bars"></i>
    </button>
    {#if visible}
        <div in:enlarge="{{duration: 500}}" out:dislarge="{{duration: 500}}">
            <NavbarElements/>
        </div>
    {/if}
</nav>
