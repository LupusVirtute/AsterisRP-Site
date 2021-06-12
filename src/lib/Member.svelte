<script lang="ts">
    import type {member} from '../configs/memberConfig';
    export let number;
    export let memberValue: member;
    let value = number%2 == 0 ? "4vw" : "10vw";
</script>
<style lang="sass">
@import '../themes/Member'
</style>
<div class="member" style="margin-right: {value};width: 80vw">
    <div class="aboutContainer">
        <h4>{memberValue.nick}</h4>
        <hr/>
        <article>
            {memberValue.about}
        </article>
    </div>
    <!-- Had to do this nightmare lmao     -->
    <div class="memberImage" style=" background: url({memberValue.image}) no-repeat; background-size: cover; background-position: 50% 50%" alt="Member"></div>
</div>