<script lang="ts">
    import Particles from "svelte-particles";
    import background from '../assets/background.json?url';
    import logo from '../assets/AsterisRP.svg';
    import backgroundImage from '../assets/Background.jpg';
	let visible = false;
    window.setTimeout(typeActivator,500);
    function typeActivator(){
        visible = !visible;
        window.setTimeout(typeActivator,5000);
    }
    function typewriter(node, { speed = 100 }) {
		const valid = (
			node.childNodes.length === 1 &&
			node.childNodes[0].nodeType === Node.TEXT_NODE
		);

		if (!valid) {
			throw new Error(`This transition only works on elements with a single text node child`);
		}

		const text = node.textContent;
		const duration = text.length * speed;

		return {
			duration,
			tick: t => {
				const i = ~~(text.length * t);
                if(t == 1)
                    node.textContent = text.slice(0,i)+'  ';
                else
				    node.textContent = text.slice(0, i)+'|';
			}
		};
	}
</script>
<style lang="sass" global>
    @import '../themes/MainLogo.sass'
</style>

<div class="visitContainer" style="background: url({backgroundImage}); background-size:cover;">
    <Particles
    id="particles"
    url="{background}"
    />
    <img class="logo" src="{logo}" alt="Logo serwera Asteris RP" />
    {#if visible}
    <h1 in:typewriter out:typewriter="{{speed: 60}}">Asteris RP</h1>
    {/if}
</div>
