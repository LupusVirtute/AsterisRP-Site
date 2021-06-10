<script lang="ts">
    export let about: string;
    export let memberImage: string;
    export let number: number;
    let value = number%2 == 0 ? "4vw" : "10vw";
</script>
<style lang="sass">
@import '../themes/Member'
</style>
<div class="member" style="margin-right: {value};width: 80vw">
    <article>
        {about}
    </article>
    <!-- Had to do this nightmare lmao     -->
    <div class="memberImage" style=" background: url({memberImage}) no-repeat; background-size: cover; background-position: 50% 50%" alt="Member"></div>
</div>