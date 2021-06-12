<script lang="ts">
    import wave from '../assets/wave.svg';
    import { members } from '../configs/memberConfig';
    import Member from './Member.svelte';
</script>
<style lang="sass">
@import '../themes/Squad.sass'
</style>
<div id="Squad">
    <img class="wave" src="{wave}" alt="fala" />
    <h2>Nasza Drużyna</h2>
    {#each members as member,i}
        <Member number="{i}" memberValue="{member}"/>
    {/each}
</div>